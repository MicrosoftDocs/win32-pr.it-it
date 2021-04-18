---
description: Il metodo set imposta il tipo di supporto da un altro tipo di supporto.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Metodo CMediaType. set (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325515"
---
# <a name="cmediatypeset-method-mtypeh"></a>Metodo CMediaType. set (mtype. h)

Il `Set` metodo imposta il tipo di supporto da un altro tipo di supporto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo copia l'intero tipo di supporto da *mtype*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




