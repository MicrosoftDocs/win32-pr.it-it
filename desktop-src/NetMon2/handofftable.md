---
description: La struttura HANDOFFTABLE definisce i protocolli di una tabella con continuità.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Struttura HANDOFFTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305890"
---
# <a name="handofftable-structure"></a>Struttura HANDOFFTABLE

La struttura **HANDOFFTABLE** definisce i protocolli di una tabella con continuità.

Questa struttura viene compilata da Network Monitor in base alle informazioni contenute in un file con estensione ini fornito dall'utente durante la chiamata della funzione [**CreateHandoffTable**](createhandofftable.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**Sig. attivo \_**
</dt> <dd>

Firma che identifica la tabella come tabella di continuità.

</dd> <dt>

**numEntries a caldo \_**
</dt> <dd>

Numero di voci che Network Monitor aggiunte alla tabella di continuità.

</dd> <dt>

**\_voci sensibili**
</dt> <dd>

Tabella con continuità.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura e le strutture HANDOFFENTRY associate vengono compilate da Network Monitor quando Network Monitor crea una tabella con continuità.

Le informazioni sul protocollo utilizzate durante la creazione di una tabella con continuità vengono fornite in un file ini fornito dall'applicazione quando viene chiamato [**CreateHandoffTable**](createhandofftable.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> </dl>

 

 




