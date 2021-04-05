---
title: Modifica di un oggetto ADSI da ADO
description: ADSI per Windows 2000 e il client DS includono un provider di OLE DB di sola lettura. Ciò significa che attualmente non è possibile eseguire l'istruzione UPDATE nel sottolinguaggio SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modifica di un oggetto ADSI da ADO ADSI
- ActiveX Data Object ADSI, modifica di un oggetto ADSI da ADO
- ADSI ADSI, esempio di codice C/C++, modifica di un oggetto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707408"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modifica di un oggetto ADSI da ADO

ADSI per Windows 2000 e il client DS includono un provider di OLE DB di sola lettura. Ciò significa che attualmente non è possibile eseguire l'istruzione UPDATE nel sottolinguaggio SQL.

**Per modificare un oggetto restituito da una query ADO**

1.  Richiedere il **ADsPath** quando si specifica un nome di attributo, come in "Select ADsPath,..."
2.  Eseguire la query e ottenere l'attributo **ADsPath** .
3.  Eseguire l'associazione al set di record utilizzando **ADsPath** e modificare gli attributi.

Nell'esempio di codice riportato di seguito viene illustrato come modificare un oggetto ADSI dopo aver eseguito i passaggi descritti nell'esempio precedente.


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



 

 




