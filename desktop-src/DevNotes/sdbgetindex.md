---
description: Recupera l'indice per il tag e il tipo di chiave specificati dal database specificato.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Funzione SdbGetIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666476"
---
# <a name="sdbgetindex-function"></a>Funzione SdbGetIndex

Recupera l'indice per il tag e il tipo di chiave specificati dal database specificato.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ Pollici\]
</dt> <dd>

The TAG.

</dd> <dt>

*tKey* \[ Pollici\]
</dt> <dd>

Tipo di chiave.

</dd> <dt>

*lpdwFlags* \[ out, facoltativo\]
</dt> <dd>

Questo parametro può essere 0 o **SHIMDB \_ INDEX \_ UNIQUE \_ KEY** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TAGID dell'indice** o **TAGID \_ NULL.**

## <a name="remarks"></a>Commenti

L'indice risultante può essere usato per le operazioni di lettura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




