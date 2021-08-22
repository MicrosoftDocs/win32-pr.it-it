---
description: Il metodo Exit segnala l'uscita del thread di streaming.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Metodo CSourceStream.Exit (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2c1c0de67eaa1067a4c72f3500674dddef65ddbb11af1b520973120d2df3c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687431"
---
# <a name="csourcestreamexit-method"></a>Metodo CSourceStream.Exit

Il `Exit` metodo segnala l'uscita del thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ UNEXPECTED.

## <a name="remarks"></a>Commenti

Il [**metodo CSourceStream::Inactive**](csourcestream-inactive.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




