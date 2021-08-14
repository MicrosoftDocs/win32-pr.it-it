---
title: Codice di esempio per la pubblicazione del punto di connessione RnR
description: L'esempio di codice seguente viene usato dal servizio Winsock per registrare il punto di connessione RnR per il servizio.
ms.assetid: dd2c7ac9-76fc-4366-8654-8048e6793a16
ms.tgt_platform: multiple
keywords:
- Codice di esempio per la pubblicazione del punto di connessione RnR AD
- Windows Registrazione e risoluzione dei socket ad , codice di esempio, pubblicazione del punto di connessione RnR
- Pubblicazione del punto di connessione RnR AD , codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a66581ea20acc42993451a8074e08f8b15f2244d4db1c997da2a978c717aaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693204"
---
# <a name="example-code-for-publishing-the-rnr-connection-point"></a>Codice di esempio per la pubblicazione del punto di connessione RnR

L'esempio di codice seguente viene usato dal servizio Winsock per registrare il punto di connessione RnR per il servizio.


```C++
#include <winsock2.h>
#include <stdio.h>

/***************************************************************************

    serverRegister()

    Registers the RnR connection point for the specified service. WSAStartup 
    must be called before calling this function.

***************************************************************************/

INT serverRegister(SOCKADDR * sa, 
                   GUID *pServiceID, 
                   LPTSTR pszServiceInstanceName, 
                   LPTSTR pszServiceInstanceComment)
{
    DWORD ret;
    WSAVERSION Version;
    WSAQUERYSET QuerySet;
    CSADDR_INFO CSAddrInfo[1];
    SOCKADDR sa_local;

    memset(&QuerySet, 0, sizeof(QuerySet));
    memset(&CSAddrInfo, 0, sizeof(CSAddrInfo));
    memset(&sa_local, 0, sizeof(SOCKADDR));
    sa_local.sa_family = AF_INET;

    // Build the CSAddrInfo structure to contain address
    // data that clients use to establish a connection.
    //
    // Be aware that LocalAddr is set to zero because dynamically
    // assigned port numbers are used.
    //
    CSAddrInfo[0].LocalAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].LocalAddr.lpSockaddr = &sa_local;
    CSAddrInfo[0].RemoteAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].RemoteAddr.lpSockaddr = sa;
    CSAddrInfo[0].iSocketType = SOCK_STREAM;
    CSAddrInfo[0].iProtocol = PF_INET;

    QuerySet.dwSize = sizeof(WSAQUERYSET);
    QuerySet.lpServiceClassId = pServiceID;
    QuerySet.lpszServiceInstanceName = pszServiceInstanceName;
    QuerySet.lpszComment = pszServiceInstanceComment;
    QuerySet.lpVersion = &Version;
    QuerySet.lpVersion->dwVersion = 2;
    QuerySet.lpVersion->ecHow = COMP_NOTLESS;
    QuerySet.dwNameSpace = NS_NTDS;
    QuerySet.dwNumberOfCsAddrs = 1;
    QuerySet.lpcsaBuffer = CSAddrInfo;

    ret = WSASetService( &QuerySet,
                         RNRSERVICE_REGISTER,
                         SERVICE_MULTIPLE);

    return(ret);
}
```



 

 




