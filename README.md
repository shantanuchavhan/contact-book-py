while True:
    inputs=input("enter what you want to do( add , delete , search ):")
    names=[]
    phone_numbers=[]
    num=3
    add="add"
    delete="delete"
    search="search"
    
    if add in inputs:
        name=input("Name:")
        phone_number=input('Phone Number:')
        names.append(name)
        phone_numbers.append(phone_number)
    if search in inputs:
        search_term=input("\n Enter search Term: ")
        print("Search Result")
        if search_term in names:
            index=names.index(search_term)
            phone_number=phone_numbers[index]
            print("Name {},Phone Number: {}".format(search_term,phone_number))
        else:
            print("name not found")
    if delete in inputs:
        remove_number=input("names please:")
        if remove_number in names:
            index=names.index(remove_number)
            del names[index]
            del phone_numbers[index]
        print(names)
        
    if "contact" in inputs:
        print(names)
