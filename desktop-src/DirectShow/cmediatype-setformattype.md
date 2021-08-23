---
description: Il metodo SetFormatType specifica il tipo di formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Metodo CMediaType.SetFormatType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954420"
---
# <a name="cmediatypesetformattype-method"></a>Metodo CMediaType.SetFormatType

Il metodo ''SetFormatType specifica il tipo di formato.

## <a name="syntax"></a>Sintassi


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pformattype* 
</dt> <dd>

Puntatore a **un GUID** che specifica il tipo di formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il **membro formattype.** Il tipo di formato definisce il layout del blocco di formato. Ad esempio, se il tipo di formato è FORMAT \_ VideoInfo, il blocco di formato deve contenere una **struttura VIDEOINFOHEADER.** Per impostare il blocco di formato, chiamare il [**metodo CMediaType::SetFormat.**](cmediatype-setformat.md) Il chiamante è responsabile della verifica che il blocco di formato corrisponda al tipo di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 


``
