---
description: Pseudoblocking pseudo blocking operations in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocco e vero blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740943"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-blocco e vero blocco

In 16 Windows, il vero blocco non è supportato dal sistema operativo. Pertanto, un'operazione di blocco che non può essere completata immediatamente viene gestita come segue:

-   Il provider di servizi avvia l'operazione e quindi entra in un ciclo durante il quale invia tutti i messaggi Windows (cedendo il processore a un altro thread, se necessario)
-   Verifica quindi il completamento della funzione Windows Sockets.
-   Se la funzione è stata completata o [**se WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) è stato richiamato, il ciclo viene terminato e la funzione di blocco viene completata con un risultato appropriato.

Questo è il significato del termine pseudo-blocco e il ciclo a cui si fa riferimento in precedenza è noto come hook di blocco predefinito.

 

 
