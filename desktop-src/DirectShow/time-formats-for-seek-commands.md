---
description: Formati di ora per i comandi Seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formati di ora per i comandi Seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e585a7dda12b40e7f501e51aff6ffed50d647066f03804c82e5ffa236f8623a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078721"
---
# <a name="time-formats-for-seek-commands"></a>Formati di ora per i comandi Seek

Molti dei metodi **nell'interfaccia IMediaSeeking** hanno parametri che esprimono valori di posizione, ad esempio la posizione corrente o la posizione di arresto. Per impostazione predefinita, questi parametri sono espressi in unità di 100 nanosecondi, denominate anche tempo di riferimento. Qualsiasi filtro che può essere cercato deve supportare la ricerca in base all'ora di riferimento. Alcuni filtri possono cercare usando anche altre unità di tempo, ad esempio la ricerca di un determinato numero di fotogramma o la ricerca di un offset di byte specificato all'interno di un flusso. Ognuna di queste unità di tempo è denominata formato di ora ed è definita da un identificatore univoco globale (GUID). Per un elenco dei formati di ora definiti da DirectShow, vedere [**GUID di formato ora**](time-format-guids.md). Terze parti possono anche definire GUID per formati di ora personalizzati.

Per determinare se i filtri attualmente presenti nel grafico dei filtri supportano un formato di ora specifico, chiamare il metodo [**IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) Il metodo restituisce S \_ OK se il formato è supportato. In caso contrario, restituisce S \_ FALSE o un codice di errore. Se è supportato un formato, è possibile passare a tale formato chiamando il [**metodo IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) Se il **metodo SetTimeFormat ha** esito positivo, i comandi seek successivi vengono espressi usando il nuovo formato dell'ora.

Nell'esempio seguente viene verificato se il grafo supporta la ricerca in base al numero di fotogramma. In tal caso, cerca di impostare il numero di fotogramma 20:


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



Si noti che i formati di ora si applicano solo ai comandi di ricerca. Non influiscono sulla riproduzione del grafo o su altre azioni.

 

 



