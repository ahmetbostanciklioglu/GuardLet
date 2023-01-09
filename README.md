# GuardLet
Guard let optional unwrapping



**Guard let unwrapping:**

func optinalParamFunc(_ optionalParameter: String? = nil) {
    guard let optionalParameter else {
        print("It is an empty optional parameter")
        return
    }
    print("it is unwrapped optional param \"\(optionalParameter)\"")
}

optinalParamFunc("Ahmet")



func optionalReturningFunc(_ param: Int?) -> String? {
    guard let param  else {
        return nil
    }
    if param == 2024 {
        return "This year"
    } else {
        return nil
    }
}

if let unwrappedOptional = optionalReturningFunc(2023) {
    print("Hi, \(unwrappedOptional)!")
}else {
    print("Unwrapped optional is \(String(describing: optionalReturningFunc(2023)))")
}

