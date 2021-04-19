---
description: Informazioni sul metodo del costruttore CMediaType. CMediaType (mtype. h). Questo metodo usa il parametro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Costruttore CMediaType. CMediaType (mtype. h)-parametro majortype
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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323832"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Costruttore CMediaType. CMediaType (mtype. h)-parametro majortype

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*majortype* 
</dt> <dd>

Puntatore a un **GUID** di tipo principale. Il costruttore inizializza il GUID del tipo principale su questo valore.

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

 

 




