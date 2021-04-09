---
description: Esecuzione di query per la ricerca di funzionalità
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Esecuzione di query per la ricerca di funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876798"
---
# <a name="querying-for-seeking-capabilities"></a>Esecuzione di query per la ricerca di funzionalità

Microsoft® DirectShow® supporta la ricerca tramite l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Il gestore del grafo del filtro espone questa interfaccia, ma la funzionalità di ricerca viene sempre implementata dai filtri nel grafico.

Non è possibile cercare alcuni dati. Ad esempio, non è possibile cercare un flusso video live da una fotocamera. Se un flusso è ricercabile, tuttavia, esistono diversi tipi di ricerca che potrebbero supportare. Tra queste sono incluse:

-   Ricerca in una posizione arbitraria nel flusso.
-   Recupero della durata del flusso.
-   Recupero della posizione corrente all'interno del flusso.
-   Riproduzione in ordine inverso.

L'interfaccia **IMediaSeeking** definisce un set di flag, [**che \_ cercano \_ \_ funzionalità di ricerca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), che descrivono le possibili funzionalità di ricerca. Per recuperare le funzionalità del flusso, chiamare il metodo [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Il metodo restituisce una combinazione bit per bit di flag. L'applicazione può testarli usando l'operatore & ( **and** bit per bit). Il codice seguente, ad esempio, controlla se il grafo può cercare in una posizione arbitraria:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



