---
title: Proprietà utente personalizzate di WinNT
description: Il provider WinNT rende disponibili le proprietà personalizzate seguenti per la classe User. È possibile accedervi tramite i metodi IADs.Get e IADs.Put. Per altre informazioni, vedere la struttura USER \_ INFO \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Proprietà utente personalizzate di WinNT ADSI
- Provider WinNT ADSI, oggetto utente, proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e12fc58ff4829f425302c1d13997f2e6c085646b1ace2c3e8ae2ebfb7df6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838390"
---
# <a name="winnt-custom-user-properties"></a>Proprietà utente personalizzate di WinNT

Il provider WinNT rende disponibili le proprietà personalizzate seguenti per la classe User. È possibile accedervi tramite i metodi [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) Per altre informazioni, vedere la [**struttura USER \_ INFO \_ 3.**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3)



| Proprietà            | Type         | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | string       | Home Directory Unità dell'utente. Si tratta di un puntatore a una stringa Unicode che specifica il percorso della home directory. La stringa può essere **Null.** Vedere l'esempio in questo argomento.                                                                                                                                                                                 |
| **ObjectSID**       | Stringa dell'ottetto | SID dell'oggetto dell'utente. Per un esempio di come recuperare il SID dell'oggetto usando il provider WinNT, vedere [Object SID (WinNT Provider) (SID oggetto (provider WinNT)](object-sid.md)                                                                                                                                                                                                          |
| **Parametri**      | string       | Parametri dell'utente. Punta a una stringa Unicode che viene accantonata per l'uso da parte delle applicazioni. Questa stringa può essere una stringa Null o può contenere un numero qualsiasi di caratteri prima del carattere Null di terminazione. I prodotti Microsoft usano questo membro per archiviare i dati di configurazione utente. Questa proprietà può essere modificata solo da un'applicazione durante l'installazione. |
| **PasswordAge**     | Ora         | Durata della password in uso. Questa proprietà indica il numero di secondi trascorsi dall'ultima modifica della password.                                                                                                                                                                                                                    |
| **PasswordExpired** | Intero      | Indica quando la password è scaduta. Quando si usa Get, verrà restituito zero se la password non è scaduta o è diversa da zero se è scaduta. Vedere l'esempio in questo argomento.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Intero      | ID del gruppo primario dell'utente, ad esempio l'ID del gruppo di utenti di dominio. Vedere l'esempio in questo argomento.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Intero      | Flag utente definito in [**ADS \_ USER FLAG \_ \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Per un esempio di come usare UserFlags, vedere [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)                                                                                                                                                             |



 

Questo esempio illustra come impostare la home directory di un utente.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Questo esempio illustra come usare PasswordExpired per forzare un utente a modificare la password all'accesso successivo.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



Questo esempio illustra come ottenere il gruppo primario dell'utente.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 