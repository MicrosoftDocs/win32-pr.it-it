---
description: Informazioni sul metodo del costruttore CMediaType. CMediaType (mtype. h). Questo metodo usa i parametri ' mtype ' è PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Costruttore CMediaType. CMediaType (mtype. h)-parametri mtype e PHR
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323830"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Costruttore CMediaType. CMediaType (mtype. h)-parametri mtype e PHR

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se disponibile.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT. Questo parametro può essere un puntatore **null** . In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore. Se il costruttore ha esito negativo, imposta il valore su un codice di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il costruttore chiama il metodo [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.

## <a name="requirements"></a>Requisiti

| Requisito                   | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Mtype. h (include Streams. h)                                                                                     |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




