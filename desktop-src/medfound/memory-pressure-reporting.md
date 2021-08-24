---
description: La creazione di report di utilizzo elevato della memoria consente a un'applicazione Direct3D di determinare quando la memoria video working set è aumentata troppo.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Creazione di report sull'utilizzo della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723771"
---
# <a name="memory-pressure-reporting"></a>Creazione di report sull'utilizzo della memoria

La creazione di report di utilizzo elevato della memoria consente a un'applicazione Direct3D di determinare quando la memoria video working set è aumentata troppo.

*La pressione della* memoria è la richiesta posta nel sottosistema di memoria da un'applicazione. Anche se qualsiasi applicazione Direct3D può usare la creazione di report sulla pressione della memoria, questa funzionalità è particolarmente utile per le applicazioni che eseguono il rendering di video usando Direct3D. La riproduzione video in genere trae vantaggio da grandi quantità di buffering, in modo che i fotogrammi possano essere decodificati in anticipo. Mentre la memorizzazione nel buffer in genere comporta una riproduzione più fluida, può effettivamente peggiorare le prestazioni se il working set aumenta troppo, a causa dei fattori seguenti:

-   È possibile che la memoria venga rimosso dalla cache. Nel peggiore dei casi, ciò può verificarsi in ogni fotogramma video.
-   Le allocazioni di memoria possono essere posizionate in segmenti di memoria nonoptimal.

A partire da Windows 7, Direct3D può segnalare alcune statistiche sulla pressione della memoria video:

-   Numero di byte sfrattati dal processo in un intervallo di tempo.
-   Quantità di memoria inserita in segmenti di memoria nonoptimal.
-   Indicazione approssimativa dell'efficienza complessiva delle allocazioni di memoria inserite nella memoria non ottimale.

Queste informazioni consentono a un'applicazione di mantenere un livello working set.

## <a name="using-memory-pressure-reporting"></a>Uso della creazione di report sull'utilizzo della memoria

La creazione di report sull'utilizzo della memoria **usa l'interfaccia IDirect3DQuery9 esistente** per eseguire query sul dispositivo. È stato aggiunto un nuovo tipo di query **all'enumerazione D3DQUERYTYPE.**


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Per usare questa query, seguire questa procedura:

1.  Chiamare **IDirect3DDevice9Ex::CreateQuery** con il flag **D3DQUERYTYPE \_ MEMORYPRESSURE.** Questo metodo restituisce un puntatore **all'interfaccia IDirect3DQuery9.**
2.  Chiamare **IDirect3DQuery9::Issue** con il flag **D3DISSUE \_ BEGIN** per iniziare l'intervallo di misurazione.
3.  Chiamare **IDirect3DQuery9::Issue** con il flag **D3DISSUE \_ END.**
4.  Chiamare **IDirect3DQuery9::GetData** per ottenere il risultato della query. La query restituisce una [**struttura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)

## <a name="example-code"></a>Codice di esempio

L'esempio seguente mostra due funzioni che misurano la pressione della memoria. Il primo inizia l'intervallo di misurazione e il secondo recupera i risultati della misura.


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

[API Video Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



