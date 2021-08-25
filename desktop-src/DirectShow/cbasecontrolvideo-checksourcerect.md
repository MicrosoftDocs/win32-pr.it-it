---
description: Determina se un rettangolo di origine è valido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Metodo CBaseControlVideo.CheckSourceRect (Ctlutil.h)
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
ms.openlocfilehash: cf7ac41d626eceee048afc4671a5e171e7164adfbd9a941b1b70bc85ea988c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873011"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>Metodo CBaseControlVideo.CheckSourceRect

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

Puntatore al rettangolo di origine da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se non è valido; in caso contrario, restituisce NOERROR (S \_ OK).

## <a name="remarks"></a>Commenti

Questa funzione membro controlla che il rettangolo di origine richiesto non superi il video di origine disponibile. Le coordinate sinistra e superiore non possono essere negative e la larghezza e l'altezza non possono superare la parte destra e inferiore del video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




