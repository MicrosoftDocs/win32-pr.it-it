---
title: Temporizzazione (Windows Multimedia)
description: Intervallo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, temporizzazione
- DrawDibTime (funzione)
- DrawDib, debug
- debug di DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474861"
---
# <a name="timing-windows-multimedia"></a>Temporizzazione (Windows Multimedia)

Come parte del debug di un'applicazione, è possibile ottenere informazioni sul tempo necessario per completare le operazioni DrawDib ripetitive. La funzione [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restituisce informazioni sulla temporizzazione per le operazioni seguenti:

-   Disegno di una bitmap
-   Decompressione di una bitmap
-   Retinatura di una bitmap
-   Estensione di una bitmap
-   Trasferimento di una bitmap tramite la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Trasferimento di una bitmap tramite la funzione [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Dopo il recupero di un set di valori, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) Reimposta il conteggio e il valore per ogni operazione.

La funzione [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) è disponibile solo nella versione di debug delle funzioni DrawDib.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di immagini](image-rendering.md)
</dt> </dl>

 

 
