# ToDoList
todo_list=[]
def show_menu():
    print("\n To-Do List Menu")
    print("1.View Tasks")
    print("2.Add Task")
    print("3.Delete Task")
    print("4.Exit")
while True:
    show_menu()
    choice=input("enter your choice(1-4)")
    if choice=='1':
        if not todo_list:
            print("No tasks yet")
        else:
            for i,task in enumerate(todo_list,1):
                print(f"{i}.{task}")
    elif choice=='2':
        task=input("enter new task:")
        todo_list.append(task)
        print("Task added!")
    elif choice=='3':
        task_no=int(input("enter task number to delete"))
        if 0<task_no<=len(todo_list):
            removed=todo_list.pop(task_no-1)
            print("Removed:f{removed}")
        else:
            print("invalid task number!")
    elif choice=='4':
            print("GoodBye!")
            break
    else:
            print("invalid choice.Try Again")
        
        
        
        
        
        
        
        
