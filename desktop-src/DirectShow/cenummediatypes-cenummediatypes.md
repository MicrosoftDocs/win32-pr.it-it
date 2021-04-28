---
description: 'Costruttore CEnumMediaTypes.CEnumMediaTypes : metodo costruttore.'
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Costruttore CEnumMediaTypes.CEnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095679"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Costruttore CEnumMediaTypes.CEnumMediaTypes

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore al pin su cui deve essere eseguita l'enumerazione.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Puntatore [**all'interfaccia IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) di un enumeratore da clonare oppure **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *pEnumMediaTypes è* **NULL,** questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione. In caso contrario, duplica lo stato interno dell'enumeratore specificato *da pEnumMediaTypes.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




