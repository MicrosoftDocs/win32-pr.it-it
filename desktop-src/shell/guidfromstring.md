---
description: Converte una stringa in un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Funzione GUIDFromString
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
ms.openlocfilehash: 38dd6d6365c3b306e63634fee02ac7add07b1bf262598efc88ffec2595e14c82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351061"
---
# <a name="guidfromstring-function"></a>Funzione GUIDFromString

\[**GUIDFromString** è disponibile tramite Windows XP con Service Pack 2 (SP2) o Windows Vista. Potrebbe essere modificato o non disponibile nelle versioni successive. Le applicazioni devono [**usare CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) o [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) al posto di questa funzione.\]

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

*psz* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore alla stringa con terminazione Null da convertire. La stringa deve essere nel formato seguente:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ Cambio\]
</dt> <dd>

Tipo: **LPGUID**

Puntatore a un buffer per ricevere il GUID quando questo metodo viene restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

**TRUE** se il GUID è stato creato correttamente. in caso contrario, **FALSE.**

## <a name="remarks"></a>Commenti

Questa funzione non viene dichiarata in un'intestazione o esportata in base al nome da un file .dll file. Deve essere caricato da un Shell32.dll come numero ordinale 703 per **GUIDFromStringA** e 704 per **GUIDFromStringW.**

È anche possibile accedervi da Shlwapi.dll come numero ordinale 269 per **GUIDFromStringA** e 270 per **GUIDFromStringW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **GUIDFromStringW** (Unicode) e **GUIDFromStringA** (ANSI)<br/>                |



 

 
