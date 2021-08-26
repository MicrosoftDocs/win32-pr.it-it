---
description: Il metodo ChangeStop viene chiamato quando cambia la posizione di arresto.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Metodo CSourceSeeking.ChangeStop (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09473b5bbe20c6c31748f0079594424f7e0afa62e2594ff1cc80f33cb1f5e6bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103121"
---
# <a name="csourceseekingchangestop-method"></a>Metodo CSourceSeeking.ChangeStop

Il `ChangeStop` metodo viene chiamato quando cambia la posizione di arresto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Il [**metodo CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione di arresto cambia. Questo metodo è virtuale puro. la classe derivata deve implementarla. L'esempio seguente illustra una possibile implementazione:


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




