---
description: Costruttore CMediaType.CMediaType (Mtype.h) - Metodo costruttore.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Costruttore CMediaType.CMediaType (Mtype.h): parametri cmtype e phr'
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
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095419"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Costruttore CMediaType.CMediaType (Mtype.h)

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

Riferimento a un `CMediaType` oggetto . Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se presente.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT. Questo parametro può essere un **puntatore NULL.** In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore. Se il costruttore ha esito negativo, imposta il valore su un codice di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il costruttore chiama il [**metodo CMediaType::InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




