---
description: La funzione DumpGraph invia informazioni su un grafico di filtro al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Funzione DumpGraph (Wxdebug. h)
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
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329359"
---
# <a name="dumpgraph-function"></a>DumpGraph (funzione)

La `DumpGraph` funzione Invia informazioni su un grafico di filtro al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.

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

Puntatore all'interfaccia [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) in gestione grafico dei filtri.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Livello di registrazione. La funzione genera un \_ messaggio di traccia del log con il livello di registrazione specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




