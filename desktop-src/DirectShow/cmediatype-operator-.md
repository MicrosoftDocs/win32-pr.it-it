---
description: "Il metodo CMediaType. CMediaType:: operator = (mtype. h) consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto."
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType:: operator = Method (mtype. h)-parametro cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323858"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a>CMediaType. CMediaType:: operator = Method (mtype. h)-parametro cmtype

Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.

## <a name="syntax"></a>Sintassi


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Riferimento a un oggetto **CMediaType** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto.

## <a name="requirements"></a>Requisiti

| Requisito                   | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Mtype. h (include Streams. h)                                                                                     |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




