---
description: La struttura PROTOCOLTABLE contiene un elenco di protocolli.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Struttura PROTOCOLTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315451"
---
# <a name="protocoltable-structure"></a>Struttura PROTOCOLTABLE

La struttura **PROTOCOLTABLE** contiene un elenco di protocolli.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**nProtocols**
</dt> <dd>

Numero di protocolli abilitati.

</dd> <dt>

**hProtocol**
</dt> <dd>

Matrice di handle per i protocolli abilitati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




