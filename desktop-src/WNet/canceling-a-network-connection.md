---
title: Annullamento di una connessione di rete
description: Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la funzione WNetCancelConnection2, come illustrato nell'esempio seguente.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872806"
---
# <a name="canceling-a-network-connection"></a>Annullamento di una connessione di rete

Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la funzione [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , come illustrato nell'esempio seguente.

La chiamata a **WNetCancelConnection2** specifica che una connessione di rete non deve più essere persistente. Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la funzione di [**testo**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.


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



La funzione [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) è supportata per la compatibilità con le versioni precedenti di Windows per gruppi di lavoro. Per le nuove applicazioni, usare [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).

 

 