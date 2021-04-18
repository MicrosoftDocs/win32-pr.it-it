---
description: 'Il metodo commit alloca la memoria per i buffer. Questo metodo implementa il metodo IMemAllocator:: commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Metodo CBaseAllocator. Commit (Amfilter. h)
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
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328271"
---
# <a name="cbaseallocatorcommit-method"></a>Metodo CBaseAllocator. commit

Il `Commit` metodo alloca la memoria per i buffer. Questo metodo implementa il metodo [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati di seguito.



| Codice restituito                                                                                       | Descrizione                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | I requisiti del buffer non sono stati specificati.<br/> |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) per specificare i requisiti del buffer.

Questo metodo chiama il metodo virtuale [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) per allocare la memoria per i buffer. Le classi derivate possono eseguire l'override di **Alloc**. Se un'operazione di decommit è in sospeso, viene annullata.

È necessario chiamare questo metodo prima di chiamare il metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




