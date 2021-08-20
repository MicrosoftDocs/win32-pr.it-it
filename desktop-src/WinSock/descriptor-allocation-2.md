---
description: Anche se Windows provider di servizi Sockets sono invitati a implementare i socket come oggetti file system (IFS) installabili, l'architettura Winsock supporta anche i provider di servizi i cui handle di socket non sono oggetti IFS.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Allocazione descrittore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0efd7d2ca1e7ed949626033b88074c591b64d52ea27cf8f3a481d2361d110c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112382"
---
# <a name="descriptor-allocation"></a>Allocazione descrittore

Anche se Windows provider di servizi Sockets sono invitati a implementare i socket come oggetti file system (IFS) installabili, l'architettura Winsock supporta anche i provider di servizi i cui handle di socket non sono oggetti IFS. I provider con handle IFS indicano questa operazione tramite il bit dell'attributo \_ XP1 IFS \_ HANDLES nella struttura [**WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) (Nota: XP1 \_ Il bit dell'attributo IFS HANDLES non è incluso nella versione 2.0.8 della specifica API, ma è stato aggiunto da allora tramite \_ il meccanismo errata. I client SPI Winsock possono sfruttare i vantaggi dei provider i cui descrittori di socket sono handle IFS usando questi descrittori con funzionalità di I/O Windows standard, ad esempio [ReadFile](/windows/win32/api/fileapi/nf-fileapi-readfile) [e WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile).

Ogni volta che un provider IFS crea un nuovo descrittore di socket, è obbligatorio che il provider chiami [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) prima di fornire il nuovo handle a un client SPI Windows Sockets. Questa funzione accetta come input un identificatore del provider e un handle IFS proposto dal provider e restituisce un handle (possibilmente) modificato. Il provider IFS deve fornire solo l'handle modificato al client e tutte le richieste dal client farà riferimento solo a questo handle modificato. È garantito che l'handle modificato sia indistinguibile dall'handle proposto per quanto riguarda il sistema operativo. Pertanto, nella maggior parte dei casi, il provider di servizi sceglierà semplicemente di usare solo l'handle modificato in tutta l'elaborazione interna. Lo scopo di questa funzione di modifica è consentire al32.dll Ws2 di semplificare notevolmente il processo di identificazione del provider di servizi associato \_ a un determinato socket.

I provider che non restituiscono handle IFS devono ottenere un handle valido dal32.dll Ws2 \_ tramite la [**chiamata WPUCreateSocketHandle.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) Il provider nonIFS deve offrire al client solo un handle fornito 2.DLL socket Windows e tutte le richieste dal client farà riferimento solo a questi handle. Per praticità per gli implementatori del provider di servizi, uno dei parametri di input forniti da un provider in **WPUCreateSocketHandle è** un valore di contesto DWORD. Il32.dll Ws2 associa questo valore di contesto all'handle del socket allocato e consente a un provider di servizi di recuperare il valore di contesto in qualsiasi momento tramite la \_ [**chiamata WPUQuerySocketHandleContext.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) Un uso tipico di questo valore di contesto è l'archiviazione di un puntatore a una struttura di dati gestita dal provider di servizi usata per archiviare le informazioni sullo stato del socket.

 

 
