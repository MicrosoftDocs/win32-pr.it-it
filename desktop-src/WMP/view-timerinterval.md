---
title: VIEW.timerInterval
description: L'attributo timerInterval specifica o recupera l'intervallo, in millisecondi, in corrispondenza del quale il timer genera eventi al gestore eventi di avvio.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- View.timerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43b2b7bbd87663a35c43db733d3e11ff0dca5bc3ddfd00e57022b4df7122c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001311"
---
# <a name="viewtimerinterval"></a>VIEW.timerInterval

**L'attributo timerInterval** specifica o recupera l'intervallo, in millisecondi, in corrispondenza del quale il timer genera eventi al gestore **eventi** di avvio.

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (**long**) con un valore predefinito di 1000.



| Valore        | Descrizione                    |
|--------------|--------------------------------|
| 0            | L'evento timer non viene generato. |
| 50 e successive | Intervallo in millisecondi.  |



 

Qualsiasi valore inferiore a 50 (inclusi i numeri negativi, ma senza zero) genera un errore e il valore precedente viene mantenuto.

## <a name="remarks"></a>Commenti

Questa operazione non viene attivata automaticamente se **non viene** implementato alcun gestore eventi di avvio. Non si verifica quindi alcuna riduzione delle prestazioni anche se il valore predefinito è diverso da zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**VIEW.ontimer**](view-ontimer.md)
</dt> </dl>

 

 





