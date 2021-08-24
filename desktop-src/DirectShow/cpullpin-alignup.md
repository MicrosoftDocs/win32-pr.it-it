---
description: Il metodo AlignUp arrotonda un valore fino a un limite di allineamento specificato. Nota Rimossa in Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Metodo CPullPin.AlignUp (Pullpin.h)
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
ms.openlocfilehash: 34c45fe4a34e21647cd976adbf29dfe6723e4216d58166e7d1599d4c8d64d47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687761"
---
# <a name="cpullpinalignup-method"></a>Metodo CPullPin.AlignUp

Il **metodo AlignUp** arrotonda un valore fino a un limite di allineamento specificato.

> [!Note]  
> Rimozione in Windows 7.

 

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
> Questo metodo può causare un overflow numerico in caso di overflow *di ll* + (*lAlign* - 1).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




