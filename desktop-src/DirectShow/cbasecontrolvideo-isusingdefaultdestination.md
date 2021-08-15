---
description: Il metodo IsUsingDefaultDestination determina se il renderer usa la finestra di destinazione predefinita.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Metodo CBaseControlVideo.IsUsingDefaultDestination (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf254ec89cc6804af86c98abaaa0c53ae5f76a25766391529ca4de85bee7d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955220"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a>Metodo CBaseControlVideo.IsUsingDefaultDestination

Il `IsUsingDefaultDestination` metodo determina se il renderer usa la finestra di destinazione predefinita.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se si usa la destinazione predefinita; in caso contrario, restituisce S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




