---
title: Configurazione di distruttori e decompressori
description: Configurazione di distruttori e decompressori
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- gestione compressione video(VCM), configurazione dei dispositivi
- VCM (Video Compression Manager), configurazione dei dispositivi
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144924"
---
# <a name="configuring-compressors-and-decompressors"></a>Configurazione di distruttori e decompressori

Nell'esempio seguente viene utilizzata la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) per illustrare come verificare se un oggetto supporta la finestra di dialogo di configurazione e come visualizzarla, se disponibile.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



L'esempio seguente illustra come ottenere i dati sullo stato usando la macro [**ICGetState.**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



L'esempio seguente illustra come ripristinare i dati sullo stato usando la macro [**ICSetState.**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) I dati sullo stato ripristinati dalle applicazioni non devono contenere modifiche ai dati di stato ottenuti da un driver.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




