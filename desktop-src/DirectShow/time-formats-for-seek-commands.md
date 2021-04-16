---
description: Formati di ora per i comandi seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formati di ora per i comandi seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530325"
---
# <a name="time-formats-for-seek-commands"></a>Formati di ora per i comandi seek

Molti dei metodi nell'interfaccia **IMediaSeeking** hanno parametri che esprimono i valori di posizione, ad esempio la posizione corrente o la posizione di arresto. Per impostazione predefinita, questi parametri sono espressi in unità di 100 nanosecondi, detti anche ora di riferimento. Qualsiasi filtro che può essere cercato deve supportare la ricerca in base all'ora di riferimento. Alcuni filtri possono essere cercati anche usando altre unità di tempo, ad esempio la ricerca di un determinato numero di frame o la ricerca di un offset di byte specificato all'interno di un flusso. Ognuna di queste unità di tempo è denominata formato ora ed è definita da un identificatore univoco globale (GUID). Per un elenco dei formati di ora definiti da DirectShow, vedere GUID del [**formato di ora**](time-format-guids.md). Le terze parti possono anche definire i GUID per i formati di ora personalizzati.

Per determinare se i filtri attualmente presenti nel grafico di filtro supportano un formato di ora specifico, chiamare il metodo [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) . Il metodo restituisce \_ OK se il formato è supportato. In caso contrario, restituisce \_ false o un codice di errore. Se un formato è supportato, è possibile passare a tale formato chiamando il metodo [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) . Se il metodo **SetTimeFormat** ha esito positivo, i comandi di ricerca successivi vengono espressi usando il nuovo formato di ora.

Nell'esempio seguente viene controllato se il grafo supporta la ricerca in base al numero di frame. In caso affermativo, Cerca il frame numero 20:


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



Si noti che i formati di ora si applicano solo ai comandi Seek. Non influiscono sulla riproduzione del grafo o su altre azioni.

 

 



