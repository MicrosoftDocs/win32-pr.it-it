---
description: Metodo costruttore che fornisce il mapping tra tipi DWORD in formato multimediale di vecchio stile e sottotipi GUID. Questo metodo usa il parametro 'Fourcc'.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - Parametro Fourcc
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
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043211"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>Costruttore FOURCCMap::FOURCCMap (Fourcc.h) - Parametro Fourcc

Metodo del costruttore. Il constuctor fornisce il mapping tra i tipi DWORD in formato **multimediale** precedente e i **sottotipi GUID.**

## <a name="syntax"></a>Sintassi


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Fourcc* 
</dt> <dd>

**Valore DWORD** che specifica FOURCC.

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

 

 




