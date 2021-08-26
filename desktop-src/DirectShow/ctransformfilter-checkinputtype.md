---
description: Il metodo CheckInputType controlla se un tipo di supporto specificato è accettabile per l'input.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Metodo CTransformFilter.CheckInputType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ef410ac8d96160b39ca9b7103e5125be8619169ba6b287a32b8769e57a0cbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053621"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Metodo CTransformFilter.CheckInputType

Il `CheckInputType` metodo verifica se un tipo di supporto specificato è accettabile per l'input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il tipo di supporto è accettabile.<br/>     |
| <dl> <dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt> </dl> | Il tipo di supporto non è accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Restituisce S \_ OK se il formato di input proposto è accettabile oppure un codice di errore in caso contrario.

Questo metodo non deve verificare che il formato di input sia compatibile con il formato di output (se presente). Il pin di input lo verifica chiamando il [**metodo CheckTransform.**](ctransformfilter-checktransform.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




