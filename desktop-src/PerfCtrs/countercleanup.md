---
description: Rimuove la registrazione dei provider.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Funzione CounterCleanup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011369"
---
# <a name="countercleanup-function"></a>Funzione CounterCleanup

Rimuove la registrazione del provider.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il provider chiama questa funzione. La funzione chiama la [**funzione PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) per rimuovere la registrazione del provider.

Lo [**strumento CTRPP**](ctrpp.md) genera questa funzione inline quando si specifica l'argomento **-o.** Il nome della funzione include una stringa *di* prefisso se si specifica l'argomento **-prefix** (ad esempio, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 




