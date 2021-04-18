---
description: Determina se un rettangolo di origine è valido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Metodo CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327583"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>CBaseControlVideo. CheckSourceRect, metodo

Determina se un rettangolo di origine è valido.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore al rettangolo di origine da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se non è valido; in caso contrario, restituisce NOERROR (S \_ OK).

## <a name="remarks"></a>Commenti

Questa funzione membro verifica che il rettangolo di origine richiesto non superi il video di origine disponibile. Le coordinate Left e Top non possono essere negative e la larghezza e l'altezza non possono superare il lato destro e inferiore del video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




