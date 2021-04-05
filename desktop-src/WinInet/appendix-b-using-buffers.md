---
title: Uso di buffer di stringa
description: Le funzioni che restituiscono stringhe contengono un parametro di input, lpszBuffer, e un parametro size, lpdwBufferLength. Sebbene lpszBuffer possa essere NULL, lpdwBufferLength deve essere un puntatore valido a una variabile DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728762"
---
# <a name="using-string-buffers"></a>Uso di buffer di stringa

Le funzioni che restituiscono stringhe contengono un parametro di input, *lpszBuffer*, e un parametro size, *lpdwBufferLength*. Sebbene *lpszBuffer* possa essere **null**, *lpdwBufferLength* deve essere un puntatore valido a una variabile **DWORD** . Se il buffer di input a cui punta *lpszBuffer* è **null** o troppo piccolo per conservare la stringa di output, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente**. La variabile a cui punta *lpdwBufferLength* contiene un numero che rappresenta il numero di byte che la funzione richiede per restituire la stringa richiesta, incluso il terminatore **null** . L'applicazione deve allocare un buffer di queste dimensioni, impostare la variabile a cui punta *lpdwBufferLength* su questo valore e inviare nuovamente la richiesta. Se la dimensione del buffer è sufficiente per ricevere la stringa richiesta, la stringa viene copiata nel buffer di output con un carattere di terminazione **null** e la funzione restituisce un'indicazione di esito positivo. La variabile a cui punta *lpdwBufferLength* ora contiene il numero di caratteri archiviati nel buffer, escluso il terminatore **null** .

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 