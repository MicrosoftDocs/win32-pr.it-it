---
description: 'Costruttore CUnknown.CUnknown : metodo costruttore.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Costruttore CUnknown.CUnknown (Combase.h)
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
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084609"
---
# <a name="cunknowncunknown-constructor"></a>Costruttore CUnknown.CUnknown

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

*Pname* 
</dt> <dd>

Stringa contenente il nome dell'oggetto. utilizzato nel costruttore [**CBaseObject per**](cbaseobject.md) il debug.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario dell'oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto viene inizializzato con un conteggio dei riferimenti pari a zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




