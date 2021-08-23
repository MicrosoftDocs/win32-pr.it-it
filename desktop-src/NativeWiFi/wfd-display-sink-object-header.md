---
description: Descrive i dati dell'oggetto sink di visualizzazione inclusi nel risultato di una notifica o di una notifica.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink.h)
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
ms.openlocfilehash: e4c9e4d83fbac1cccb2dbc0643acc707176be433dfca7854395a0f97c9c36435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800471"
---
# <a name="wfd_display_sink_object_header-structure"></a>Struttura DELL'INTESTAZIONE \_ \_ DELL'OGGETTO SINK DISPLAY \_ WFD \_

La **struttura WFD \_ DISPLAY SINK OBJECT \_ \_ \_ HEADER** descrive i dati dell'oggetto sink di visualizzazione inclusi in un risultato di notifica o notifica.

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

Tipo dell'oggetto sink di visualizzazione. È possibile usare **l'identificatore WFD \_ DISPLAY SINK OBJECT TYPE \_ \_ \_ \_ DEFAULT,** definito come valore 1.

</dd> <dt>

**Revisione**
</dt> <dd>

Versione di revisione dell'oggetto sink di visualizzazione. È possibile usare **l'identificatore WFD \_ DISPLAY SINK OBJECT REVISION VERSION \_ \_ \_ \_ \_ 1,** definito come valore 1.

</dd> <dt>

**Length**
</dt> <dd>

Lunghezza dei dati nel risultato della notifica o della notifica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




