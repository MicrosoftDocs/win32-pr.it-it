---
description: Rimuove la registrazione dei provider.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup (funzione)
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
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312182"
---
# <a name="countercleanup-function"></a>CounterCleanup (funzione)

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

Il provider chiama questa funzione. La funzione chiama la funzione [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) per rimuovere la registrazione del provider.

Lo strumento [**CTRPP**](ctrpp.md) genera questa funzione inline quando si specifica l'argomento **-o** . Il nome della funzione include una stringa di *prefisso* se si specifica l'argomento **-Prefix** , ad esempio **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 




