---
description: Il metodo AlignUp Arrotonda un valore fino a un limite di allineamento specificato. Nota rimossa in Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Metodo CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328491"
---
# <a name="cpullpinalignup-method"></a>CPullPin. AlignUp, metodo

Il metodo **AlignUp** Arrotonda un valore fino a un limite di allineamento specificato.

> [!Note]  
> Rimosso in Windows 7.

 

## <a name="syntax"></a>Sintassi


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ll* 
</dt> <dd>

Specifica il numero da allineare.

</dd> <dt>

*lAlign* 
</dt> <dd>

Specifica il limite di allineamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il risultato allineato.

## <a name="remarks"></a>Commenti

> [!Caution]  
> Questo metodo può causare un overflow numerico se *ll* + (*lAlign* -1) si verifica in overflow.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




