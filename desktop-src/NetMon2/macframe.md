---
description: La struttura MACFRAME è un'unione dei protocolli iniziali più comuni.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Unione MACFRAME (Netmon.h)
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
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364709"
---
# <a name="macframe-union"></a>Unione MACFRAME

La **struttura MACFRAME** è un'unione dei protocolli iniziali più comuni.

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

Puntatore dell'anello di token a un frame.

</dd> <dt>

**Fddi**
</dt> <dd>

Puntatore FDDI a un frame.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata più frequentemente come sovrimpressione. Per rendere accessibili le proprietà del primo protocollo, eseguire il cast del frame dello stesso tipo del protocollo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




