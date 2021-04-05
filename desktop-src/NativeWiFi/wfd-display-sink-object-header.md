---
description: Descrive i dati dell'oggetto sink di visualizzazione inclusi in un risultato di notifica o di notifica.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Struttura WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881453"
---
# <a name="wfd_display_sink_object_header-structure"></a>\_Struttura dell' \_ \_ intestazione dell'oggetto sink di visualizzazione della direttiva. \_

La struttura dell' **\_ \_ \_ \_ intestazione dell'oggetto sink di visualizzazione della direttiva GMA** descrive i dati dell'oggetto sink di visualizzazione inclusi nei risultati di una notifica o di una notifica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo dell'oggetto sink di visualizzazione. È possibile utilizzare il valore **\_ predefinito del \_ \_ tipo di \_ oggetto \_ sink di visualizzazione** dell'identificatore, definito come valore 1.

</dd> <dt>

**Revisione**
</dt> <dd>

Versione di revisione dell'oggetto sink di visualizzazione. È possibile usare l'identificatore **di \_ visualizzazione del sink di visualizzazione dell' \_ \_ oggetto sink \_ \_ versione \_ 1** , definito come valore 1.

</dd> <dt>

**Length**
</dt> <dd>

Lunghezza dei dati nel risultato della notifica o della notifica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




