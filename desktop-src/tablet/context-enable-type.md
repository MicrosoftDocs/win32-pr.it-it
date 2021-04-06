---
description: Indica se i messaggi di contesto devono essere inviati alla routine della finestra proprietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumerazione CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758855"
---
# <a name="context_enable_type-enumeration"></a>\_Enumerazione del tipo abilitata per il contesto \_

Indica se i messaggi di contesto devono essere inviati alla routine della finestra proprietaria.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_Abilita contesto**
</dt> <dd>

È necessario abilitare il contesto della tavoletta, in modo da inviare messaggi di contesto alla routine della finestra proprietaria.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**\_disabilitazione del contesto**
</dt> <dd>

Il contesto del tablet deve essere disabilitato, impedendo l'invio di altri messaggi di contesto alla routine della finestra o al sink di evento della finestra proprietaria.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ITablet:: CreateContext**](itablet-createcontext.md)
</dt> </dl>

 

 




