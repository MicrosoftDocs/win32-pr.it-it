---
title: Visualizza timerInterval
description: L'attributo timerInterval specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- Visualizza Media Player Windows timerInterval
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325115"
---
# <a name="viewtimerinterval"></a>Visualizza timerInterval

L'attributo **timerInterval** specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi **OnTimer** .

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore predefinito di 1000.



| Valore        | Descrizione                    |
|--------------|--------------------------------|
| 0            | L'evento timer non viene attivato. |
| 50 e versioni successive | Intervallo in millisecondi.  |



 

Qualsiasi valore inferiore a 50 (inclusi i numeri negativi, ma non incluso zero) genera un errore e viene mantenuto il valore precedente.

## <a name="remarks"></a>Commenti

Questa operazione non viene eseguita automaticamente se non viene implementato alcun gestore eventi **OnTimer** . In questo modo non si verifica alcun calo delle prestazioni, anche se il valore predefinito è diverso da zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Visualizza. OnTimer**](view-ontimer.md)
</dt> </dl>

 

 





