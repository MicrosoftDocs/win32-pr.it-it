---
description: Metodo costruttore che fornisce il mapping tra tipi DWORD in formato multimediale di vecchio stile e sottotipi GUID. Questo metodo usa il parametro 'pguid'.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - parametro pguid
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
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330441"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - parametro pguid

Metodo del costruttore. Il constuctor fornisce il mapping tra i tipi DWORD in formato **multimediale** precedente e i **sottotipi GUID.**

## <a name="syntax"></a>Sintassi


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguid* 
</dt> <dd>

Puntatore all'identificatore univoco globale (**GUID**).

</dd> </dl>

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

 

 




