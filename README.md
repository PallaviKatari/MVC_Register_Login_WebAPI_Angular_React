# MVC_Register_Login_WebAPI_Angular_React

DATABASE
--------
CREATE DATABASE MVC_API_LOGIN_REGISTER

USE MVC_API_LOGIN_REGISTER

CREATE TABLE [dbo].[EmployeeLogin](    
    [Id] [int] IDENTITY(1,1) NOT NULL,    
    [Email] [varchar](50) NULL,    
    [Password] [varchar](50) NULL,    
    [EmployeeName] [varchar](50) NULL,    
    [City] [varchar](50) NULL,    
    [Department] [varchar](50) NULL,    
 CONSTRAINT [PK_EmployeeLogin] PRIMARY KEY CLUSTERED     
(    
    [Id] ASC    
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]    
) ON [PRIMARY]    
    
GO    

ENABLE CORS TO ACCESS API IN ANGULAR/REACT - WebApiConfig.cs
-------------------------------------------------------------
 //Enable CORS
            EnableCorsAttribute cors = new EnableCorsAttribute("http://localhost:4200,http://localhost:3000", "*", "*");
            config.EnableCors(cors);
