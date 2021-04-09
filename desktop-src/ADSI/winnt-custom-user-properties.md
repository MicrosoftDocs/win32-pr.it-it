---
title: Proprietà utente personalizzate WinNT
description: Il provider WinNT rende disponibili le seguenti proprietà personalizzate per la classe utente. È possibile accedervi tramite i metodi IADs. Get e IADs. Put. Per ulteriori informazioni, vedere la \_ struttura User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Proprietà utente personalizzate WinNT ADSI
- ADSI del provider WinNT, oggetto utente, proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963459"
---
# <a name="winnt-custom-user-properties"></a>Proprietà utente personalizzate WinNT

Il provider WinNT rende disponibili le seguenti proprietà personalizzate per la classe utente. È possibile accedervi tramite i metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) . Per ulteriori informazioni, vedere la struttura [**User \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .



| Proprietà            | Type         | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | string       | Unità Home directory dell'utente. Si tratta di un puntatore a una stringa Unicode che specifica il percorso della Home Directory. La stringa può essere **null**. Vedere l'esempio in questo argomento.                                                                                                                                                                                 |
| **ObjectSID**       | Stringa ottetto | SID oggetto dell'utente. Per un esempio di come recuperare il SID dell'oggetto utilizzando il provider WinNT, vedere [oggetto SID (provider WinNT)](object-sid.md)                                                                                                                                                                                                          |
| **Parametri**      | string       | Parametri dell'utente. Punta a una stringa Unicode riservata per l'utilizzo da parte delle applicazioni. Questa stringa può essere una stringa null oppure può contenere un numero qualsiasi di caratteri prima del carattere null di terminazione. I prodotti Microsoft usano questo membro per archiviare i dati di configurazione dell'utente. Questa proprietà può essere modificata solo da un'applicazione durante l'installazione. |
| **Password**     | Tempo         | Durata dell'intervallo di tempo per la password in uso. Questa proprietà indica il numero di secondi trascorsi dall'Ultima modifica della password.                                                                                                                                                                                                                    |
| **PasswordExpired** | Integer      | Indica quando la password è scaduta. Quando si usa Get, viene restituito zero se la password non è scaduta o è diverso da zero se è scaduta. Vedere l'esempio in questo argomento.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Integer      | ID gruppo primario dell'utente, ad esempio ID gruppo utenti di dominio. Vedere l'esempio in questo argomento.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Integer      | Flag utente definito nell' [**\_ enumerazione del \_ flag \_ utente ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Per un esempio di come usare UserFlags, vedere [Nessuna scadenza password (provider WinNT)](winnt-password-never-expires.md)                                                                                                                                                             |



 

Questo esempio illustra come impostare la directory dell'unità principale di un utente.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Questo esempio illustra come usare PasswordExpired per forzare l'utente a modificare la password all'accesso successivo.


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



 

 