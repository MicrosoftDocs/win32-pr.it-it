---
description: La struttura ADDRESSTABLE contiene una tabella di coppie di indirizzi.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Struttura ADDRESSTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064281"
---
# <a name="addresstable-structure"></a>Struttura ADDRESSTABLE

La **struttura ADDRESSTABLE** contiene una tabella di coppie di indirizzi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**nAddressPairs**
</dt> <dd>

Numero di coppie di indirizzi nella **matrice AddressPair.**

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

Numero di coppie di indirizzi non MAC.

</dd> <dt>

**AddressPair**
</dt> <dd>

Matrice di coppie di indirizzi. Si noti che è possibile archiviare fino a otto coppie di indirizzi per ogni struttura ADDRESSTABLE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa struttura come parte del processo di costruzione del filtro di acquisizione. Per altre informazioni sull'implementazione di questa struttura, vedere [Acquisizione di filtri](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




