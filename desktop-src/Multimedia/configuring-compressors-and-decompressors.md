---
title: Configurazione di comprimer e decompressori
description: Configurazione di comprimer e decompressori
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Gestione compressione video (VCM), configurazione di compressatori
- VCM (Gestione compressione video), configurazione dei commediatori
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395830"
---
# <a name="configuring-compressors-and-decompressors"></a>Configurazione di comprimer e decompressori

Nell'esempio seguente viene utilizzata la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) per illustrare come verificare se un compressore supporta la finestra di dialogo di configurazione e per visualizzarlo in caso contrario.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



Nell'esempio seguente viene illustrato come ottenere i dati di stato utilizzando la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



Nell'esempio seguente viene illustrato come ripristinare i dati di stato utilizzando la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) . I dati di stato ripristinati dalle applicazioni non devono contenere modifiche ai dati dello stato ottenuti da un driver.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




