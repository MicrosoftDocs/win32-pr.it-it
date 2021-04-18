---
description: Metodo del costruttore.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Costruttore CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
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
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329855"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Costruttore CEnumMediaTypes. CEnumMediaTypes

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

Puntatore al pin sul quale deve essere eseguita l'enumerazione.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) di un enumeratore da clonare o **null**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *pEnumMediaTypes* è **null**, questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione. In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumMediaTypes*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




