---
description: Classe padre per gli eventi di intestazione del log. Questa classe è sempre la prima classe di traccia eventi inviata a un consumer (questo evento non viene inviato ai consumer in tempo reale). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Classe EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977671"
---
# <a name="eventtraceevent-class"></a>Classe EventTraceEvent

Classe padre per gli eventi di intestazione del log. Questa classe è sempre la prima classe di traccia eventi inviata a un consumer (questo evento non viene inviato ai consumer in tempo reale).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **EventTraceEvent** non definisce membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**\_Intestazione EventTrace**](eventtrace-header.md)
</dt> </dl>

 

 




