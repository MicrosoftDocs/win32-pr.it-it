---
description: Il metodo AlterQuality notifica al filtro che è richiesta una modifica di qualità.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Metodo CTransformFilter. AlterQuality (Transfrm. h)
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
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325737"
---
# <a name="ctransformfilteralterquality-method"></a>CTransformFilter. AlterQuality, metodo

Il `AlterQuality` metodo notifica al filtro che è richiesta una modifica di qualità.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*d* 
</dt> <dd>

Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il messaggio di qualità non è stato gestito. Il messaggio deve essere passato a Monte.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Ha gestito il messaggio qualitativo. Non sono richieste ulteriori azioni.<br/>               |



 

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo se il filtro è in grado di eseguire il controllo qualità. Per altre informazioni, vedere [gestione del controllo di qualità](quality-control-management.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




