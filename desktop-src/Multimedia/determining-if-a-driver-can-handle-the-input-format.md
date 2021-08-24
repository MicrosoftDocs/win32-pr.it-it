---
title: Determinare se un driver è in grado di gestire il formato di input
description: Determinare se un driver è in grado di gestire il formato di input
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- gestione compressione video(VCM), formato di input
- VCM (Gestione compressione video),formato di input
- Macro ICDrawQuery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497291"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Determinare se un driver è in grado di gestire il formato di input

Nell'esempio seguente viene illustrato come controllare il formato di input con la macro [**ICDrawQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery)


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




