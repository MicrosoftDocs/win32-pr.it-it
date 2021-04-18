---
description: Metodo del costruttore.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Costruttore CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329634"
---
# <a name="cdispparamscdispparams-constructor"></a>Costruttore CDispParams. CDispParams

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nArgs* 
</dt> <dd>

Numero di argomenti passati al metodo o alla proprietà.

</dd> <dt>

*pArgs* 
</dt> <dd>

Puntatore all'elenco di argomenti. Nell'elenco ogni argomento viene archiviato con il tipo Variant.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDispParams**](cdispparams.md)
</dt> </dl>

 

 




