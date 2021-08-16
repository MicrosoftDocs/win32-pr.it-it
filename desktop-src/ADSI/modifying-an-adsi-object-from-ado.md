---
title: Modifica di un oggetto ADSI da ADO
description: ADSI per Windows 2000 e DS Client include un provider di OLE DB di sola lettura. Ciò significa che attualmente non è possibile eseguire l'istruzione UPDATE nel SQL dialetto.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modifica di un oggetto ADSI da ADO ADSI
- ActiveX oggetto dati ADSI , modifica di un oggetto ADSI da ADO
- ADSI ADSI , codice di esempio C/C++, modifica di un oggetto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839451"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modifica di un oggetto ADSI da ADO

ADSI per Windows 2000 e DS Client include un provider di OLE DB di sola lettura. Ciò significa che attualmente non è possibile eseguire l'istruzione UPDATE nel SQL dialetto.

**Per modificare un oggetto restituito da una query ADO**

1.  Richiedere **ADsPath quando** si specifica un nome di attributo, come in "SELECT ADsPath, ..."
2.  Eseguire la query e ottenere **l'attributo ADsPath.**
3.  Eseguire l'associazione al set di record **usando ADsPath** e modificare gli attributi.

Nell'esempio di codice seguente viene illustrato come modificare un oggetto ADSI dopo aver eseguito i passaggi descritti nell'esempio precedente.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




