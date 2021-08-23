---
description: Il metodo IsUsingDefaultSource determina se il renderer usa la finestra di origine predefinita.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Metodo CBaseControlVideo.IsUsingDefaultSource (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dce06ffa85b3736eca17f1ecb8303a41afb142fcc8b0d369e1f264a0cf47b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955210"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>Metodo CBaseControlVideo.IsUsingDefaultSource

Il `IsUsingDefaultSource` metodo determina se il renderer usa la finestra di origine predefinita.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il renderer usa l'origine predefinita; in caso contrario, restituisce S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




