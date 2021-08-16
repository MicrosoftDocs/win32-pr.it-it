---
description: La funzione DumpGraph invia informazioni su un grafo di filtro al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Funzione DumpGraph (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac09cc3381ab1b5f85f523d1c822768b3e2f87b6bcf08f1877680349072c216
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820960"
---
# <a name="dumpgraph-function"></a>Funzione DumpGraph

La `DumpGraph` funzione invia informazioni su un grafico di filtro al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntatore [**all'interfaccia IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) nel gestore del grafico del filtro.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Livello di registrazione. La funzione genera un messaggio LOG \_ TRACE con il livello di registrazione specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




