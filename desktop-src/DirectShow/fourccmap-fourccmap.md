---
description: Metodo costruttore che fornisce il mapping tra tipi DWORD in formato multimediale di vecchio stile e sottotipi GUID. Questo metodo non usa parametri.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - Nessun parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d856589146103e599a1cf67d2090dd64af7107d1c221c46b9c93852f989ade9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015729"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - Nessun parametro

Metodo del costruttore. Il constuctor fornisce il mapping tra i tipi DWORD in formato **multimediale** precedente e i **sottotipi GUID.**

## <a name="syntax"></a>Sintassi


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parametri

Questo costruttore non ha parametri.

## <a name="remarks"></a>Commenti

Se questo oggetto viene costruito con il **codice FOURCC,** viene creato un **GUID** per la corrispondenza. Se questo oggetto viene creato con un **GUID esistente,** il **valore FOURCC** dell'oggetto viene impostato su zero. Successivamente, il **valore FOURCC** può essere impostato o recuperato usando rispettivamente le funzioni membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC.**](fourccmap-getfourcc.md)

## <a name="requirements"></a>Requisiti


| Requisito | Valore |
|-|-|
| Intestazione  | Fourcc.h (include Flussi.h) |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




