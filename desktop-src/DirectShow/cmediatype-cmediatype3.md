---
description: Informazioni sul metodo CMediaType.CMediaType constructor (Mtype.h). Questo metodo usa i parametri 'mtype' e 'phr'.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Costruttore CMediaType.CMediaType (Mtype.h) - parametri mtype e phr
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
ms.openlocfilehash: 0c399073794f025122e1cfade3f15b3a96784f28e171482e4dcfb7bcec6a8271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084481"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Costruttore CMediaType.CMediaType (Mtype.h) - parametri mtype e phr

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

Riferimento a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se presente.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT. Questo parametro può essere un **puntatore NULL.** In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore. Se il costruttore ha esito negativo, imposta il valore su un codice di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il costruttore chiama il [**metodo CMediaType::InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.

## <a name="requirements"></a>Requisiti

| Requisito                   | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Mtype.h (includere Flussi.h)                                                                                     |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




