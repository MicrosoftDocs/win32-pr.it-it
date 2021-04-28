---
description: 'Metodo CBaseOutputPin.Active: il metodo Active notifica al pin che il filtro è ora attivo.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Metodo CBaseOutputPin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096209"
---
# <a name="cbaseoutputpinactive-method"></a>Metodo CBaseOutputPin.Active

Il `Active` metodo notifica al pin che il filtro è ora attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                          | Descrizione                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Operazione completata.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::Active.**](cbasepin-active.md) Chiama il [**metodo IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) nell'allocatore per allocare memoria per i buffer.

Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




