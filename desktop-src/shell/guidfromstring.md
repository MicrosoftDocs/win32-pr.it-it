---
description: Converte una stringa in un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881582"
---
# <a name="guidfromstring-function"></a>GUIDFromString (funzione)

\[**GUIDFromString** è disponibile tramite Windows XP con Service Pack 2 (SP2) o Windows Vista. Potrebbe essere modificato o non disponibile nelle versioni successive. Le applicazioni devono utilizzare [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) o [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) al posto di questa funzione.\]

Converte una stringa in un GUID.

## <a name="syntax"></a>Sintassi


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PSZ* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore alla stringa con terminazione null da convertire. Il formato della stringa deve essere il seguente:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ out\]
</dt> <dd>

Tipo: **LPGUID**

Puntatore a un buffer per ricevere il GUID quando il metodo restituisce un risultato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

**True** se il GUID è stato creato correttamente; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questa funzione non è dichiarata in un'intestazione o esportata in base al nome da un file con estensione dll. Deve essere caricata da Shell32.dll come ordinale 703 per **GUIDFromStringA** e ordinale 704 per **GUIDFromStringW**.

È anche possibile accedervi da Shlwapi.dll come ordinale 269 per **GUIDFromStringA** e ordinale 270 per **GUIDFromStringW**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **GUIDFromStringW** (Unicode) e **GUIDFromStringA** (ANSI)<br/>                |



 

 
