---
description: 'Costruttore CDispParams.CDispParams : metodo costruttore.'
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Costruttore CDispParams.CDispParams (Ctlutil.h)
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
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095789"
---
# <a name="cdispparamscdispparams-constructor"></a>Costruttore CDispParams.CDispParams

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

Puntatore all'elenco di argomenti. Nell'elenco ogni argomento viene archiviato con il relativo tipo variant.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDispParams**](cdispparams.md)
</dt> </dl>

 

 




