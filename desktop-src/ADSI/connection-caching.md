---
title: Connessione Caching
description: Quando viene stabilita una connessione a un server, l'handle di connessione viene memorizzato nella cache del computer client per tale processo fino a quando tale connessione non viene chiusa.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- memorizzazione nella cache delle connessioni ADSI
- memorizzazione nella cache delle connessioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fbf63d65a6941e986069289db201a237deb9ddc7058f291218c1496d0a40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429028"
---
# <a name="connection-caching"></a>Connessione Caching

Quando viene stabilita una connessione a un server, l'handle di connessione viene memorizzato nella cache del computer client per tale processo fino a quando tale connessione non viene chiusa. Se lo stesso server, la stessa porta e le stesse credenziali vengono usati in una connessione successiva e solo i flag di autenticazione **ADS \_ FAST \_ BIND** o **ADS \_ SERVER \_ BIND** differiscono, ADSI riuserà la connessione esistente. ADSI esegue la memorizzazione nella cache delle connessioni in base al processo.

Per migliorare le prestazioni, riutilizzare le connessioni esistenti quando possibile.

Nell'esempio di codice seguente viene illustrato il funzionamento della memorizzazione nella cache delle connessioni.


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




