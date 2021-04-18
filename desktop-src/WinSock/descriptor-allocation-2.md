---
description: Sebbene i provider di servizi Windows Sockets siano invitati a implementare i socket come oggetti installabili file system (IFS), l'architettura Winsock consente inoltre di gestire i provider di servizi i cui handle di socket non sono oggetti IFS.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Allocazione descrittore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306998"
---
# <a name="descriptor-allocation"></a>Allocazione descrittore

Sebbene i provider di servizi Windows Sockets siano invitati a implementare i socket come oggetti installabili file system (IFS), l'architettura Winsock consente inoltre di gestire i provider di servizi i cui handle di socket non sono oggetti IFS. I provider con handle IFS indicano questo problema tramite il \_ bit dell'attributo XP1 IFS \_ Handles nella struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . (Nota: XP1 \_ Il \_ bit dell'attributo di gestione IFS non è stato incluso nella versione 2.0.8 della specifica dell'API, ma è stato aggiunto dal meccanismo degli errori. I client Winsock SPI possono sfruttare i provider i cui descrittori di socket sono handle IFS usando questi descrittori con le funzionalità di I/O standard di Windows, ad esempio [ReadFile](/windows/win32/api/fileapi/nf-fileapi-readfile) e [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile).

Ogni volta che un provider IFS crea un nuovo descrittore di socket, è obbligatorio che il provider chiami [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) prima di fornire il nuovo handle a un client Windows Sockets SPI. Questa funzione accetta un identificatore del provider e un handle IFS proposto dal provider come input e restituisce un handle (possibilmente) modificato. Il provider IFS deve fornire solo l'handle modificato per il client e tutte le richieste dal client faranno riferimento solo a questo handle modificato. L'handle modificato è sicuramente indistinguibile dall'handle proposto per quanto riguarda il sistema operativo. Nella maggior parte dei casi, pertanto, il provider di servizi sceglierà semplicemente di utilizzare solo l'handle modificato in tutta l'elaborazione interna. Lo scopo di questa funzione di modifica consiste nel consentire all' \_32.dll WS2 di semplificare significativamente il processo di identificazione del provider di servizi associato a un socket specificato.

I provider che non restituiscono handle IFS devono ottenere un handle valido da WS2 \_32.dll tramite la chiamata [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) . Il provider nonIFS deve offrire al client solo un handle di Windows Sockets 2.DLL fornito e tutte le richieste dal client faranno riferimento solo a questi handle. Per praticità degli implementatori del provider di servizi, uno dei parametri di input forniti da un provider in **WPUCreateSocketHandle** è un valore di contesto DWORD. WS2 \_32.dll associa questo valore di contesto all'handle del socket allocato e consente a un provider di servizi di recuperare il valore di contesto in qualsiasi momento tramite la chiamata [**WPUQuerySocketHandleContext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) . Un utilizzo tipico di questo valore di contesto consiste nell'archiviare un puntatore a una struttura di dati gestita del provider di servizi utilizzata per archiviare le informazioni sullo stato del socket.

 

 
