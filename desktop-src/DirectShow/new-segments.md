---
description: Nuovi segmenti
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuovi segmenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28701a29a3b4edd61e9eb408aeab744297eac56408c49dc77dd4328a5afd24b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790931"
---
# <a name="new-segments"></a>Nuovi segmenti

Un *segmento è* un gruppo di campioni multimediali che condividono un'ora di inizio, un'ora di arresto e una frequenza di riproduzione comuni. Il [**metodo IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) segnala l'inizio di un nuovo segmento. Consente a un filtro di origine di informare i filtri downstream che le informazioni relative a tempo e frequenza sono state modificate. Ad esempio, se il filtro di origine cerca un nuovo punto nel flusso, chiama **NewSegment** con la nuova ora di inizio.

Alcuni filtri downstream usano le informazioni sui segmenti durante l'elaborazione dei campioni. Ad esempio, in un formato che usa la compressione tra frame, se l'ora di arresto rientra in un frame differenziale, il filtro di origine potrebbe dover inviare campioni aggiuntivi dopo l'ora di arresto. Ciò consente al decodificatore di decodificare il frame delta finale. Per determinare il frame finale corretto, il decodificatore fa riferimento all'ora di arresto del segmento. Come altro esempio, i renderer audio usano la frequenza dei segmenti insieme alla frequenza di campionamento audio per generare l'output audio corretto.

Nel modello push il filtro di origine avvia la **chiamata NewSegment.** Nel modello pull questa operazione viene eseguita dal filtro del parser. In entrambi i casi, il filtro chiama **NewSegment** sul pin di input downstream, che propaga la chiamata al filtro successivo, fino a quando la chiamata non raggiunge il renderer. I filtri devono serializzare **le chiamate NewSegment** con altre chiamate di streaming, ad [**esempio IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

L'ora del flusso viene reimpostata su zero dopo ogni nuovo segmento. I timestamp sui campioni recapitati dopo il segmento iniziano da zero.

 

 



