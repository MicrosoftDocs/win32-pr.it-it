---
description: La struttura EXPERTFRAMEDESCRIPTOR contiene informazioni su un frame. Quando l'esperto chiama la funzione ExpertGetFrame correttamente, Network Monitor passa nuovamente la struttura EXPERTFRAMEDESCRIPTOR all'esperto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Struttura EXPERTFRAMEDESCRIPTOR (Netmon. h)
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
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484340"
---
# <a name="expertframedescriptor-structure"></a>Struttura EXPERTFRAMEDESCRIPTOR

La struttura **EXPERTFRAMEDESCRIPTOR** contiene informazioni su un frame. Quando l'esperto chiama la funzione [**ExpertGetFrame**](expertgetframe.md) correttamente, network monitor passa nuovamente la struttura **EXPERTFRAMEDESCRIPTOR** all'esperto.

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

**NumeroFrame**
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

Se l'esperto specifica le \_ proprietà di associazione dei flag \_ quando si chiama [**ExpertGetFrame**](expertgetframe.md), il membro **szPropertyText** in ogni struttura [**PROPERTYINST**](propertyinst.md) è **null**.

Se l'esperto non specifica le proprietà di associazione dei flag \_ \_ quando chiama la funzione [**ExpertGetFrame**](expertgetframe.md) , il membro **lpPropertyTable** è **null** alla restituzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




