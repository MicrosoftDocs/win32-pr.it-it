---
description: La struttura EXPERTFRAMEDESCRIPTOR contiene informazioni su un frame. Quando l'esperto chiama correttamente la funzione ExpertGetFrame, Network Monitor passa di nuovo la struttura EXPERTFRAMEDESCRIPTOR all'esperto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Struttura EXPERTFRAMEDESCRIPTOR (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a11c131188cdd5230d309a6ff2e39a77ac7886333dafd9860d565fdcb10efc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939028"
---
# <a name="expertframedescriptor-structure"></a>Struttura EXPERTFRAMEDESCRIPTOR

La **struttura EXPERTFRAMEDESCRIPTOR** contiene informazioni su un frame. Quando l'esperto [**chiama correttamente la funzione ExpertGetFrame,**](expertgetframe.md) Network Monitor la struttura **EXPERTFRAMEDESCRIPTOR** all'esperto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Members

<dl> <dt>

**FrameNumber**
</dt> <dd>

Numero di un frame specificato.

</dd> <dt>

**hFrame**
</dt> <dd>

Handle per un frame.

</dd> <dt>

**pFrame**
</dt> <dd>

Puntatore a un frame non elaborato.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Tabella che indica dove ogni parser identifica l'inizio dei dati.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Tabella delle proprietà del frame identificate dal parser.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se l'esperto specifica FLAGS ATTACH PROPERTIES quando chiama \_ \_ [**ExpertGetFrame,**](expertgetframe.md)il membro **szPropertyText** in ogni [**struttura PROPERTYINST**](propertyinst.md) è **NULL.**

Se l'esperto non specifica FLAGS ATTACH PROPERTIES quando chiama la funzione \_ \_ [**ExpertGetFrame,**](expertgetframe.md) il membro **lpPropertyTable** è **NULL** al momento della restituzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




