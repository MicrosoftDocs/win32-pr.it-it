---
description: Flussi facoltativi
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Flussi facoltativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303889"
---
# <a name="optional-streams"></a>Flussi facoltativi

Un DMO può designare alcuni dei flussi di output come facoltativi. Un flusso facoltativo genera dati che l'applicazione può rimuovere, completamente o in caso di esempi occasionali. Ad esempio, un flusso facoltativo potrebbe contenere informazioni aggiuntive su un flusso primario.

Per eseguire una query sull'eventuale presenza di un flusso facoltativo, chiamare il metodo [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) e controllare il parametro *pdwFlags* . I flussi facoltativi restituiscono il \_ flag di output DMO \_ STREAMF \_ o il \_ \_ flag STREAMF facoltativo di output DMO \_ . Questi flag indicano quasi la stessa cosa. una differenza secondaria tra di essi verrà illustrata a breve.

Se un flusso è facoltativo, il client può indicare a DMO di rimuovere i dati dal flusso quando elabora l'output. A tale scopo, chiamare il metodo [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) e impostare il buffer di output su **null** per ogni flusso che si desidera eliminare. Il buffer di output viene specificato nel membro **pbuffer** del [**\_ \_ \_ buffer dei dati di output DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer). Impostare anche l' \_ output del processo DMO \_ \_ \_ se \_ non è presente alcun \_ flag del buffer nel parametro *dwFlags* .

Per ogni flusso in cui il puntatore *pbuffer* è **null**, DMO tenterà di eliminare i dati. Se il flusso è facoltativo, è garantito che l'oggetto DMO elimini i dati. Se il flusso non è facoltativo, DMO Elimina i dati quando possibile, ma non è garantito. Se non è possibile rimuovere i dati, imposta il \_ flag di output DMO \_ \_ BUFFERF data \_ . Se si imposta un puntatore *pbuffer* su **null** ma non si imposta l'output del processo DMO per l' \_ \_ \_ eliminazione \_ quando non è \_ presente alcun \_ flag del buffer, DMO non rimuove i dati. In tal caso, l'oggetto DMO memorizza nel buffer l'output internamente o semplicemente non riesce a eseguire la chiamata **ProcessOutput** .

L'unica differenza funzionale tra il \_ \_ flag STREAMF di output DMO \_ e il flag di \_ output DMO STREAMF facoltativo \_ \_ è la seguente:

-   Il \_ flag di output DMO \_ STREAMF \_ facoltativo indica che il client non deve impostare un tipo di supporto su tale flusso. Tuttavia, se il client inizia a elaborare i dati senza impostare il tipo di supporto per il flusso, deve eliminare i dati dal flusso per l'intera durata del flusso. Se si desidera rimuovere gli esempi in modo selettivo, è necessario impostare il tipo di supporto.
-   Il \_ flag di output DMO \_ STREAMF \_ indica che, anche se il flusso è facoltativo, richiede sempre un tipo di supporto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



