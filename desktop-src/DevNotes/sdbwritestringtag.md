---
description: Scrive una stringa nel database specificato.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877530"
---
# <a name="sdbwritestringtag-function"></a>SdbWriteStringTag (funzione)

Scrive una stringa nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
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

TAG per la voce. Questo TAG deve essere di tipo **tag \_ \_ STRINGREF**.

</dd> <dt>

*pwszData* \[ in\]
</dt> <dd>

Stringa con terminazione null. Questo parametro non può essere **null**.

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

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




