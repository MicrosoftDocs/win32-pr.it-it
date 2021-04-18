---
description: La funzionalità di creazione di report con utilizzo intensivo della memoria consente a un'applicazione Direct3D di determinare quando il working set di memoria video è troppo grande.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Segnalazione di utilizzo intensivo della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309632"
---
# <a name="memory-pressure-reporting"></a>Segnalazione di utilizzo intensivo della memoria

La funzionalità di creazione di report con utilizzo intensivo della memoria consente a un'applicazione Direct3D di determinare quando il working set di memoria video è troppo grande.

Il numero di richieste di *memoria* è la richiesta effettuata nel sottosistema di memoria da un'applicazione. Sebbene qualsiasi applicazione Direct3D possa usare la funzionalità di creazione di report con utilizzo intensivo della memoria, questa funzionalità è particolarmente utile per le applicazioni che eseguono il rendering video usando Direct3D. La riproduzione video in genere trae vantaggio da grandi quantità di buffering, in modo che sia possibile decodificare i frame in anticipo. Sebbene il buffering generi una riproduzione più uniforme, può influire negativamente sulle prestazioni in caso di dimensioni eccessive del working set, a causa dei seguenti fattori:

-   La memoria potrebbe essere rimossa dalla cache. Nel peggiore dei casi, questo problema può verificarsi in ogni fotogramma video.
-   Le allocazioni di memoria possono essere inserite in segmenti di memoria non ottimali.

A partire da Windows 7, Direct3D può segnalare alcune statistiche relative al numero di richieste di memoria video:

-   Numero di byte rimossi dal processo in un intervallo di tempo.
-   Quantità di memoria posizionata in segmenti di memoria non ottimali.
-   Indicazione approssimativa dell'efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale.

Queste informazioni consentono a un'applicazione di mantenere un working set ragionevole.

## <a name="using-memory-pressure-reporting"></a>Uso della segnalazione con utilizzo intensivo della memoria

La creazione di report con utilizzo intensivo della memoria usa l'interfaccia **IDirect3DQuery9** esistente per eseguire query sul dispositivo. È stato aggiunto un nuovo tipo di query all'enumerazione **D3DQUERYTYPE** .


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Per usare questa query, seguire questa procedura:

1.  Chiamare **IDirect3DDevice9Ex:: CreateQuery** con il **flag \_ MEMORYPRESSURE di D3DQUERYTYPE** . Questo metodo restituisce un puntatore all'interfaccia **IDirect3DQuery9** .
2.  Chiamare **IDirect3DQuery9:: Issue** con il **flag \_ Begin di D3DISSUE** per iniziare l'intervallo di misurazione.
3.  Chiamare **IDirect3DQuery9:: Issue** con il **flag \_ finale D3DISSUE** .
4.  Chiamare **IDirect3DQuery9:: GetData** per ottenere il risultato della query. La query restituisce una struttura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

## <a name="example-code"></a>Codice di esempio

Nell'esempio seguente vengono illustrate due funzioni che misurano la pressione della memoria. Il primo inizia l'intervallo di misurazione e il secondo recupera i risultati della misurazione.


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



