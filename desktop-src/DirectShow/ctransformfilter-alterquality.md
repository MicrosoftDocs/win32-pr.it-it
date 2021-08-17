---
description: Il metodo AlterQuality notifica al filtro che è richiesta una modifica di qualità.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Metodo CTransformFilter.AlterQuality (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b9b136217c23f64bcd779f5c96189ca993646ffb29ce5316cf5913de8c9abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317151"
---
# <a name="ctransformfilteralterquality-method"></a>Metodo CTransformFilter.AlterQuality

Il `AlterQuality` metodo notifica al filtro che è richiesta una modifica di qualità.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*D* 
</dt> <dd>

[**Struttura di**](/windows/win32/api/strmif/ns-strmif-quality) qualità che contiene il messaggio di controllo qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il messaggio di qualità non è stato gestito. Il messaggio deve essere passato a monte.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Gestione del messaggio di qualità. Non sono richieste ulteriori azioni.<br/>               |



 

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo se il filtro può eseguire il controllo di qualità. Per altre informazioni, vedere [Quality-Control Management](quality-control-management.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




