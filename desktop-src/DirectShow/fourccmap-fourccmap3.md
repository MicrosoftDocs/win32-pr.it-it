---
description: Metodo del costruttore che fornisce il mapping tra i tipi DWORD di formato multimediale obsoleti e i sottotipi GUID. Questo metodo usa il parametro ' pguid '.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-parametro pguid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323844"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Costruttore FOURCCMap:: FOURCCMap (fourcc. h)-parametro pguid

Metodo del costruttore. Costruttore fornisce il mapping tra i tipi **DWORD** di formato multimediale obsoleti e i sottotipi **GUID** .

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

Se questo oggetto viene costruito con il codice **fourcc** , viene creato un **GUID** corrispondente. Se questo oggetto viene creato con un **GUID** esistente, il valore **fourcc** dell'oggetto viene impostato su zero. Successivamente, è possibile impostare o recuperare il valore **fourcc** usando rispettivamente le funzioni membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione  | FourCC. h (include Streams. h) |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




