---
description: Il metodo CheckTransform controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Metodo CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329151"
---
# <a name="ctransformfilterchecktransform-method"></a>CTransformFilter. CheckTransform, metodo

Il `CheckTransform` metodo verifica se un tipo di supporto di input è compatibile con un tipo di supporto di output.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di input.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | I tipi di supporto sono compatibili.<br/>     |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | I tipi di supporto non sono compatibili.<br/> |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Restituisce \_ OK se il filtro è in grado di accettare entrambi i tipi di supporto specificati o un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




