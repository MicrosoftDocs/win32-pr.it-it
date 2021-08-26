---
description: Il metodo Commit alloca la memoria per i buffer. Questo metodo implementa il metodo IMemAllocator::Commit.
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Metodo CBaseAllocator.Commit (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087581"
---
# <a name="cbaseallocatorcommit-method"></a>Metodo CBaseAllocator.Commit

Il `Commit` metodo alloca la memoria per i buffer. Questo metodo implementa il [**metodo IMemAllocator::Commit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nell'elenco seguente.



| Codice restituito                                                                                       | Descrizione                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | I requisiti del buffer non sono stati specificati.<br/> |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare il [**metodo CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) per specificare i requisiti del buffer.

Questo metodo chiama il metodo virtuale [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) per allocare la memoria per i buffer. Le classi derivate possono eseguire **l'override di Alloc.** Se un'operazione di decommit è in sospeso, viene annullata.

È necessario chiamare questo metodo prima di chiamare [**il metodo CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




