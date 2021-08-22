---
description: Windows Sockets 2 continua a supportare tutte le semantiche e le chiamate di funzione Windows Sockets 1.1, ad eccezione di quelle che gestiscono pseudo-blocco.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Problemi di compatibilità dei socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051469"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Problemi di compatibilità dei socket

Windows Sockets 2 continua a supportare tutte le semantiche e le chiamate di funzione Windows Sockets 1.1, ad eccezione di quelle che gestiscono pseudo-blocco. Poiché Windows Sockets 2 viene eseguito solo in ambienti a 32 bit pianificati preventivamente, non è necessario implementare lo pseudo-blocco disponibile in Windows Sockets 1.1. Ciò significa che il codice di errore WSAEINPROGRESS non verrà mai indicato e che le funzioni Windows Sockets 1.1 seguenti non sono disponibili per le applicazioni Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows I programmi Sockets 1.1 scritti per utilizzare lo pseudo-blocco continueranno a funzionare correttamente perché si collegano a Winsock.dll o Wsock32.dll. Entrambi continuano a supportare il set completo di funzioni Windows Sockets 1.1. Perché i programmi diventino applicazioni Windows Sockets 2, è necessario apportare alcune modifiche al codice. Nella maggior parte dei casi, l'uso abile dei thread può essere sostituito per supportare l'elaborazione eseguita con una funzione hook di blocco.

 

 



