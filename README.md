# DataAnnotationsExample
MOD06_DEMO_02

Ejemplo del uso de **DataAnnotations**, que nos permite personalizar el modelo de datos mediante el uso de atributos que especifican reglas de formato, validación y asignación de base de datos.

public class User  

    {  
        public int UserId { get; set; }  
        
        
        [Display(Name = "Full Name:")]
        public string FullName { get; set; }  
        

        [Display(Name = "Email Address:")]
        [DataType(DataType.EmailAddress)]
        public string Email { get; set; } 
        
        public DateTime Birthdate { get; set; }

        [Display(Name = "Password:")]
        [DataType(DataType.Password)]
        public string Password { get; set; }
    }

Para trabajar con DataAnnotations, deberemos agregar un ensamblado a las referencias de nuestro proyecto. Este ensamblado es System.ComponentModel.DataAnnotations 
(Proporciona clases de atributos que se usan para definir los metadatos para ASP.NET MVC y los controles de ASP.NET).

Existen varios data anotations, los cuales puedes utilizar para realizar las validaciones, a continuación una lista con los mas comunes:

Required: El campo tiene que llenarse obligatoriamente  

Range: Define un valor máximo y mínimo en valores numéricos  

DisplayName: Especifica el nombre al mostrar para el campo  

MinLength: Indica el largo mínimo de una cadena de texto  

MaxLength: Indica el largo máximo de una cadena de texto  

EmailAddress: Valida que la cadena sea un email valido en su formato 
