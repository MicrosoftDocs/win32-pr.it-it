---
description: Informazioni sul metodo del costruttore CMediaType.CMediaType (Mtype.h). Questo metodo usa il parametro 'majortype'.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Costruttore CMediaType.CMediaType (Mtype.h) - parametro majortype
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
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073995"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Costruttore CMediaType.CMediaType (Mtype.h) - parametro majortype

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo principale* 
</dt> <dd>

Puntatore a un GUID di **tipo principale.** Il costruttore inizializza il GUID del tipo principale su questo valore.

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

 

 




