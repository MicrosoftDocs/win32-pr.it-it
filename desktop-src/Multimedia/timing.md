---
title: Intervallo (Windows Multimediali)
description: Intervallo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, intervallo
- Funzione DrawDibTime
- DrawDib, debug
- debug di DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688081"
---
# <a name="timing-windows-multimedia"></a>Intervallo (Windows Multimediali)

Come parte del debug di un'applicazione, è possibile ottenere informazioni sulla quantità di tempo necessaria per completare operazioni DrawDib ripetitive. La [**funzione DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restituisce informazioni sull'intervallo per le operazioni seguenti:

-   Disegno di una bitmap
-   Decompressione di una bitmap
-   Dithering di una bitmap
-   Estensione di una bitmap
-   Trasferimento di una bitmap tramite la [**funzione BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Trasferimento di una bitmap tramite la [**funzione StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Dopo il recupero di un set di valori, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) reimposta il conteggio e il valore per ogni operazione.

La [**funzione DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) è disponibile solo nella versione di debug delle funzioni DrawDib.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering delle immagini](image-rendering.md)
</dt> </dl>

 

 
