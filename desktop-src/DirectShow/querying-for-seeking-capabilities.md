---
description: Esecuzione di query per la ricerca di funzionalità
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Esecuzione di query per la ricerca di funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1d4389d9e5fcf1466a039ae48bbffb2c26a41c29281101984f6a7a291789f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747451"
---
# <a name="querying-for-seeking-capabilities"></a>Esecuzione di query per la ricerca di funzionalità

Microsoft® DirectShow® supporta la ricerca tramite [**l'interfaccia IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Gestione filtri Graph espone questa interfaccia, ma la funzionalità di ricerca viene sempre implementata dai filtri nel grafico.

Non è possibile cercare alcuni dati. Ad esempio, non è possibile cercare un flusso video live da una fotocamera. Se un flusso è ricercabile, tuttavia, esistono vari tipi di ricerca che potrebbero supportare. Queste includono:

-   Ricerca di una posizione arbitraria nel flusso.
-   Recupero della durata del flusso.
-   Recupero della posizione corrente all'interno del flusso.
-   Riproduzione inversa.

**L'interfaccia IMediaSeeking** definisce un set di flag, [**AM \_ \_ SEEKING SEEKING \_ CAPABILITIES,**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)che descrivono le possibili funzionalità di ricerca. Per recuperare le funzionalità del flusso, chiamare il [**metodo IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) Il metodo restituisce una combinazione bit per bit di flag. L'applicazione può testarli usando l'operatore & **(AND** bit per bit). Ad esempio, il codice seguente controlla se il grafo può cercare una posizione arbitraria:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



