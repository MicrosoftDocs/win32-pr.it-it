---
description: Scrive un valore QWORD nel database specificato.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: SdbWriteQWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748090"
---
# <a name="sdbwriteqwordtag-function"></a>SdbWriteQWORDTag (funzione)

Scrive un valore **QWORD** nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tTag* \[ in\]
</dt> <dd>

TAG per la voce. Questo TAG deve essere di tipo **tag \_ \_ QWORD**.

</dd> <dt>

*qwData* \[ in\]
</dt> <dd>

Valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




