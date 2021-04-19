---
description: Metodo del costruttore.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Costruttore CMediaType. CMediaType (mtype. h)-parametri cmtype e PHR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389065"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Costruttore CMediaType. CMediaType (mtype. h)

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Riferimento a un `CMediaType` oggetto. Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se disponibile.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT. Questo parametro può essere un puntatore **null** . In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore. Se il costruttore ha esito negativo, imposta il valore su un codice di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il costruttore chiama il metodo [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




