---
description: Informazioni sul metodo del costruttore CMediaPosition.CMediaPosition (Ctlutil.h). Questo metodo usa i parametri 'pName' e 'pUnk'.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Costruttore CMediaPosition.CMediaPosition (Ctlutil.h) - pName, parametri pUnk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634796"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Costruttore CMediaPosition.CMediaPosition (Ctlutil.h) - parametri pName, pUnk

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto, a scopo di debug. Allocare questo parametro nella memoria statica.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto oppure **NULL** se l'oggetto non è aggregato.

</dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Ctlutil.h (include Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




