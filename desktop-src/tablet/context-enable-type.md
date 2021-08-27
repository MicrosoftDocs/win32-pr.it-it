---
description: Indica se i messaggi di contesto devono essere inviati alla routine della finestra proprietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE enumerazione
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
ms.openlocfilehash: 94bffba211f75416ccae5e9a55342441b7b11b41b1a9f1f4b085ec190f991645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110971"
---
# <a name="context_enable_type-enumeration"></a>Enumerazione CONTEXT \_ ENABLE \_ TYPE

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

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT \_ ENABLE**
</dt> <dd>

Il contesto del tablet deve essere abilitato, determinando l'invio di messaggi di contesto alla routine della finestra proprietaria.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT \_ DISABLE**
</dt> <dd>

Il contesto del tablet deve essere disabilitato, impedendo l'invio di altri messaggi di contesto alla routine della finestra o al sink di evento della finestra proprietaria.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ITablet::CreateContext**](itablet-createcontext.md)
</dt> </dl>

 

 




