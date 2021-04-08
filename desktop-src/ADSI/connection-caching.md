---
title: Caching della connessione
description: Quando si effettua una connessione a un server, l'handle di connessione viene memorizzato nella cache del computer client per tale processo fino alla chiusura della connessione.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- ADSI Caching della connessione
- Caching della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d102a52be9c7ccf40f9076892a85d5b3b8683
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044069"
---
# <a name="connection-caching"></a>Caching della connessione

Quando si effettua una connessione a un server, l'handle di connessione viene memorizzato nella cache del computer client per tale processo fino alla chiusura della connessione. Se in una connessione successiva vengono utilizzati lo stesso server, la stessa porta e le stesse credenziali, ma solo i flag di autenticazione binding **\_ veloce \_** o **ADS del \_ server \_ ADS** sono diversi, ADSI riutilizzerà la connessione esistente. ADSI esegue la memorizzazione nella cache della connessione in base al processo.

Per migliorare le prestazioni, riutilizzare le connessioni esistenti, quando possibile.

Nell'esempio di codice seguente viene illustrato il funzionamento della memorizzazione nella cache della connessione.


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



 

 




