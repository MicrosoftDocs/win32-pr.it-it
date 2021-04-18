---
description: Il metodo IsPartiallySpecified determina se il tipo di supporto è parzialmente definito. Un tipo di supporto è parziale se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Metodo CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330680"
---
# <a name="cmediatypeispartiallyspecified-method"></a>CMediaType. IsPartiallySpecified, metodo

Il `IsPartiallySpecified` metodo determina se il tipo di supporto è parzialmente definito. Un tipo di supporto è *parziale* se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il tipo di supporto è parzialmente specificato. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) può accettare tipi di supporti parziali.

L'implementazione non esegue effettivamente il test del sottotipo. Se è presente un tipo di formato specificato, il tipo di supporto non viene considerato parziale, anche se il sottotipo è \_ null GUID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




