---
title: Annullamento di una connessione di rete
description: Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la funzione WNetCancelConnection2, come illustrato nell'esempio seguente.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566921"
---
# <a name="canceling-a-network-connection"></a>Annullamento di una connessione di rete

Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la [**funzione WNetCancelConnection2,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) come illustrato nell'esempio seguente.

La chiamata a **WNetCancelConnection2** specifica che una connessione di rete non deve più essere persistente. Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la [**funzione TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



La [**funzione WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) è supportata per la compatibilità con le versioni precedenti di Windows per i gruppi di lavoro. Per le nuove applicazioni, usare [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Per altre informazioni sull'uso di un gestore degli errori definito dall'applicazione, vedere [Recupero di errori di rete.](retrieving-network-errors.md)

 

 