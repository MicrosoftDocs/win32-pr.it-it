---
description: Indica un tipo di modifica dello stato del servizio per il monitoraggio e la creazione di report.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumerazione SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318222"
---
# <a name="sc_event_type-enumeration"></a>Enumerazione del tipo di \_ evento SC \_

Indica un tipo di modifica dello stato del servizio per il monitoraggio e la creazione di report.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ modifica database eventi \_ SC**
</dt> <dd>

Un servizio è stato aggiunto o eliminato. Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per SCM.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_ \_ modifica proprietà evento \_ SC**
</dt> <dd>

Una o più proprietà del servizio sono state aggiornate. Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per il servizio.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_ \_ modifica dello stato dell'evento SC \_**
</dt> <dd>

Lo stato di un servizio è stato modificato. Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per il servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl> |



 

 




