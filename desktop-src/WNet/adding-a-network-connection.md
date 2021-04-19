---
title: Aggiunta di una connessione di rete
description: Per creare una connessione a una risorsa di rete descritta da una struttura NETRESOURCE, un'applicazione può chiamare WNetAddConnection2, WNetAddConnection3 o WNetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300192"
---
# <a name="adding-a-network-connection"></a>Aggiunta di una connessione di rete

Per creare una connessione a una risorsa di rete descritta da una struttura [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , un'applicazione può chiamare [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)o [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) . Nell'esempio seguente viene illustrato l'utilizzo della funzione **WNetAddConnection2** .

Nell'esempio di codice viene chiamata la funzione **WNetAddConnection2** , specificando che il sistema deve aggiornare il profilo dell'utente con le informazioni, creando una connessione "memorizzata" o permanente. Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la funzione di [**testo**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



La funzione [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) è supportata per la compatibilità con le versioni precedenti di Windows per gruppi di lavoro. Le nuove applicazioni devono chiamare la funzione [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o la funzione [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .

Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).

 

 