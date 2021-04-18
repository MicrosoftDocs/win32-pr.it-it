---
description: Nuovi segmenti
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuovi segmenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303736"
---
# <a name="new-segments"></a>Nuovi segmenti

Un *segmento* è un gruppo di esempi di supporti che condividono un'ora di inizio, un'ora di arresto e una velocità di riproduzione comuni. Il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) segnala l'inizio di un nuovo segmento. Fornisce un modo per un filtro di origine per informare i filtri downstream che sono state modificate le informazioni relative a ora e frequenza. Se, ad esempio, il filtro di origine cerca un nuovo punto nel flusso, viene chiamato **NewSegment** con la nuova ora di inizio.

Alcuni filtri downstream utilizzano le informazioni sul segmento quando elaborano gli esempi. Ad esempio, in un formato che usa la compressione interframe, se l'ora di arresto si trova su un frame differenziale, il filtro di origine potrebbe dover inviare campioni aggiuntivi dopo l'ora di arresto. Ciò consente al decodificatore di decodificare il frame Delta finale. Per determinare il fotogramma finale corretto, il decodificatore fa riferimento all'ora di arresto del segmento. Come altro esempio, i renderer audio usano la frequenza dei segmenti insieme alla frequenza di campionamento audio per generare l'output audio corretto.

Nel modello push, il filtro di origine avvia la chiamata **NewSegment** . Nel modello pull questa operazione viene eseguita dal filtro del parser. In entrambi i casi, il filtro chiama **NewSegment** sul pin di input downstream, che propaga la chiamata al filtro successivo, finché la chiamata non raggiunge il renderer. I filtri devono serializzare le chiamate **NewSegment** con altre chiamate di streaming, ad esempio [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).

Il flusso temporale viene reimpostato su zero dopo ogni nuovo segmento. Timestamp per gli esempi recapitati dopo l'inizio del segmento da zero.

 

 



