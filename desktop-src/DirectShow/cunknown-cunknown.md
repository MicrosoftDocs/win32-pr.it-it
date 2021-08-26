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
ms.openlocfilehash: f7d2f1b70202200c705394790bb4b1e8d81349b71f534cc36fba9a8baed65f03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998931"
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

Stringa contenente il nome dell'oggetto. usato nel costruttore [**CBaseObject**](cbaseobject.md) per il debug.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto viene inizializzato con un conteggio dei riferimenti pari a zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




