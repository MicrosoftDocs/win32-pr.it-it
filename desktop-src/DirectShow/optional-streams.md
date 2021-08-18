---
description: Facoltativo Flussi
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Facoltativo Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7c30f783a8c13b00020c2dac62cd11e2a79d6f2ea66af01f715c3cb389853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830971"
---
# <a name="optional-streams"></a>Facoltativo Flussi

Un DMO può designare alcuni dei flussi di output come facoltativi. Un flusso facoltativo produce dati che l'applicazione può eliminare, completamente o su campioni occasionali. Ad esempio, un flusso facoltativo potrebbe contenere informazioni aggiuntive su un flusso primario.

Per verificare se un flusso è facoltativo, chiamare il metodo [**IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) e controllare il *parametro pdwFlags.* I flussi facoltativi restituiscono il flag DMO OUTPUT STREAMF DISCARDABLE o il \_ \_ flag DMO OUTPUT \_ \_ \_ STREAMF \_ OPTIONAL. Questi flag hanno quasi lo stesso significato. una piccola differenza tra di essi verrà illustrata a breve.

Se un flusso è facoltativo, il client può indicare al DMO di rimuovere i dati da tale flusso quando elabora l'output. A tale scopo, chiamare il [**metodo IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) e impostare il buffer di output su **NULL** per ogni flusso che si vuole rimuovere. Il buffer di output è specificato nel **membro pBuffer** dell'DMO [**OUTPUT DATA \_ \_ \_ BUFFER.**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) Impostare anche il DMO \_ PROCESS OUTPUT DISCARD WHEN NO BUFFER nel parametro \_ \_ \_ \_ \_ *dwFlags.*

Per ogni flusso in cui il *puntatore pBuffer* è **NULL,** DMO tenterà di rimuovere i dati. Se il flusso è facoltativo, DMO è garantito che scarti i dati. Se il flusso non è facoltativo, DMO elimina i dati quando possibile, ma non è garantito. Se non è in grado di rimuovere i dati, imposta DMO \_ flag OUTPUT \_ DATA \_ BUFFERF \_ INCOMPLETE. Se si imposta un *puntatore pBuffer* su **NULL** ma non si imposta il flag DMO PROCESS OUTPUT DISCARD WHEN NO BUFFER, il DMO non rimuove \_ i \_ \_ \_ \_ \_ dati. In tal caso, il DMO buffer l'output internamente o semplicemente non riesce la **chiamata a ProcessOutput.**

L'unica differenza funzionale tra il flag DMO OUTPUT STREAMF OPTIONAL e il \_ \_ flag DMO OUTPUT \_ \_ \_ STREAMF \_ DISCARDABLE è la seguente:

-   Il flag DMO OUTPUT STREAMF OPTIONAL indica che il client non deve impostare un tipo di supporto \_ \_ in tale \_ flusso. Tuttavia, se il client inizia a elaborare i dati senza impostare il tipo di supporto per tale flusso, deve rimuovere i dati da tale flusso per l'intera durata del flusso. Se si desidera eliminare i campioni in modo selettivo, è necessario impostare il tipo di supporto.
-   Il flag DMO OUTPUT STREAMF DISCARDABLE indica che, anche se il flusso è facoltativo, richiede \_ sempre un tipo di \_ \_ supporto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



