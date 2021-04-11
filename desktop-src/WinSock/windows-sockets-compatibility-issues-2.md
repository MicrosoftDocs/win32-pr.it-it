---
description: Windows Sockets 2 continua a supportare tutte le chiamate di funzione e la semantica di Windows Sockets 1,1, ad eccezione di quelle che si occupano di pseudo-blocco.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemi di compatibilità di Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226483"
---
# <a name="windows-sockets-compatibility-issues"></a>Problemi di compatibilità di Windows Sockets

Windows Sockets 2 continua a supportare tutte le chiamate di funzione e la semantica di Windows Sockets 1,1, ad eccezione di quelle che si occupano di pseudo-blocco. Poiché Windows Sockets 2 viene eseguito solo in ambienti a 32 bit e pianificati preventivamente, non è necessario implementare lo pseudo-blocco trovato in Windows Sockets 1,1. Ciò significa che il codice di errore WSAEINPROGRESS non verrà mai indicato e che le funzioni di Windows Sockets 1,1 seguenti non sono disponibili per le applicazioni Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

I programmi Windows Sockets 1,1 scritti per utilizzare lo pseudo-blocco continueranno a funzionare correttamente perché si collegano a Winsock.dll o Wsock32.dll. Entrambe continuano a supportare il set completo di funzioni Windows Sockets 1,1. Per consentire ai programmi di diventare applicazioni Windows Sockets 2, è necessario che si verifichino alcune modifiche al codice. Nella maggior parte dei casi, l'uso oculato dei thread può essere sostituito per supportare l'elaborazione eseguita con una funzione hook di blocco.

 

 



