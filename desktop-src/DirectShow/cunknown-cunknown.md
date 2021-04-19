---
description: Metodo del costruttore.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Costruttore CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326165"
---
# <a name="cunknowncunknown-constructor"></a>Costruttore CUnknown. CUnknown

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* 
</dt> <dd>

Stringa contenente il nome dell'oggetto. usato nel costruttore [**CBaseObject**](cbaseobject.md) per il debug.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto viene inizializzato con un conteggio dei riferimenti pari a zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




