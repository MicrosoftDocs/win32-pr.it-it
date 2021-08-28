---
description: Il metodo IsPartiallySpecified determina se il tipo di supporto è parzialmente definito. Un tipo di supporto è parziale se il tipo principale, il sottotipo o il tipo di formato è GUID \_ NULL.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Metodo CMediaType.IsPartiallySpecified (Mtype.h)
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
ms.openlocfilehash: 2c2e7bdbbc43195222b4054f71ec05ebe3c8a7e15ac8c634d57fba61e45bf319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084471"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Metodo CMediaType.IsPartiallySpecified

Il `IsPartiallySpecified` metodo determina se il tipo di supporto è parzialmente definito. Un tipo di supporto *è parziale* se il tipo principale, il sottotipo o il tipo di formato è GUID \_ NULL.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il tipo di supporto è parzialmente specificato. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Il [**metodo IPin::Connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) può accettare tipi di supporti parziali.

L'implementazione non testa effettivamente il sottotipo. Se è presente un tipo di formato specificato, il tipo di supporto non viene considerato parziale, anche se il sottotipo è GUID \_ NULL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




