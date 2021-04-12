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
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="30333-106">Configurazione di comprimer e decompressori</span><span class="sxs-lookup"><span data-stu-id="30333-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="30333-107">Nell'esempio seguente viene utilizzata la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) per illustrare come verificare se un compressore supporta la finestra di dialogo di configurazione e per visualizzarlo in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="30333-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="30333-108">Nell'esempio seguente viene illustrato come ottenere i dati di stato utilizzando la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="30333-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="30333-109">Nell'esempio seguente viene illustrato come ripristinare i dati di stato utilizzando la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="30333-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="30333-110">I dati di stato ripristinati dalle applicazioni non devono contenere modifiche ai dati dello stato ottenuti da un driver.</span><span class="sxs-lookup"><span data-stu-id="30333-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




