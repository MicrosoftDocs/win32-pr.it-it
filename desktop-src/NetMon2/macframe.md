---
description: La struttura MACFRAME è un'Unione dei protocolli iniziali più comuni.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Unione MACFRAME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307715"
---
# <a name="macframe-union"></a>Unione MACFRAME

La struttura **MACFRAME** è un'Unione dei protocolli iniziali più comuni.

## <a name="syntax"></a>Sintassi


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Members

<dl> <dt>

**MacHeader**
</dt> <dd>

Puntatore generico a un frame.

</dd> <dt>

**Ethernet**
</dt> <dd>

Puntatore Ethernet a un frame.

</dd> <dt>

**Tokenring**
</dt> <dd>

Puntatore all'anello token a un frame.

</dd> <dt>

**FDDI**
</dt> <dd>

Puntatore FDDI a un frame.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata con maggiore frequenza come sovrapposizione. Per rendere accessibili le proprietà del primo protocollo, eseguire il cast del frame come lo stesso tipo del protocollo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




