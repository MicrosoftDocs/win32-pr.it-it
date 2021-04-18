---
description: Recupera l'indice per il tag e il tipo di chiave specificati dal database specificato.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex (funzione)
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
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483229"
---
# <a name="sdbgetindex-function"></a>SdbGetIndex (funzione)

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

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ in\]
</dt> <dd>

TAG.

</dd> <dt>

*tKey* \[ in\]
</dt> <dd>

Tipo di chiave.

</dd> <dt>

*lpdwFlags* \[ out, facoltativo\]
</dt> <dd>

Questo parametro può essere 0 o **la \_ \_ \_ chiave univoca dell'indice SHIMDB** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** dell'indice o **TagId \_ null**.

## <a name="remarks"></a>Commenti

L'indice risultante può essere utilizzato per le operazioni di lettura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




