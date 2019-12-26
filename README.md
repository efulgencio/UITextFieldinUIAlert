# UITextFieldinUIAlert
How to add UITextField to UIAlert (iOs - Swift)

```
      var textFieldAlert = UITextField()
        // Crecion del alert controller
        let alert = UIAlertController(title: "Lista de Tareas.", message: "", preferredStyle: .alert)

        // Accion de añadir
        let action = UIAlertAction(title: "Añadir", style: .default) {  (action) in
            // Recuperamos el contenido introducido en textFieldAlert
            debugPrint(textFieldAlert.text as Any)
        }
        alert.addTextField { ( textField ) in
            // Configuramos el text field
            textField.placeholder = "Introduce una tarea."
            textField.layer.borderColor = UIColor.gray.cgColor
            textField.layer.borderWidth = 0.5
            // asignar al text field fuera del ambito
            textFieldAlert = textField
        }
        alert.addAction(action)
        // Accion de cancelar
        let cancelar = UIAlertAction(title: "Cancelar", style: .destructive )
        alert.addAction(cancelar)
        // Mostrar el alert con el uitextfield
        present(alert, animated: true, completion: nil)

```

