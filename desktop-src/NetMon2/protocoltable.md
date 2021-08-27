---
description: La struttura PROTOCOLTABLE contiene un elenco di protocolli.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Struttura PROTOCOLTABLE (Netmon.h)
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
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036981"
---
# <a name="protocoltable-structure"></a>Struttura PROTOCOLTABLE

La **struttura PROTOCOLTABLE** contiene un elenco di protocolli.

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




