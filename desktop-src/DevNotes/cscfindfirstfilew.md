---
description: Cerca un file nella cache File offline che soddisfi i criteri specificati.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Funzione CSCFindFirstFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 7289fb19a0062ce66212927bbe3e77c9e90c54ceb1980f83265000cc228e27ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833411"
---
# <a name="cscfindfirstfilew-function"></a>Funzione CSCFindFirstFileW

\[Questa funzione non è supportata e non deve essere usata.\]

Cerca un file nella cache File offline che soddisfi i criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszFileName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un percorso o una directory UNC valida.

</dd> <dt>

*lpFind32* \[ Cambio\]
</dt> <dd>

Puntatore alla struttura [**WIN32 \_ FIND \_ DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) che riceve informazioni sul file o sulla sottodirectory.

</dd> <dt>

*lpdwStatus* \[ Cambio\]
</dt> <dd>

Codice NTSTATUS che indica lo stato della chiamata.

</dd> <dt>

*lpdwPinCount* \[ Cambio\]
</dt> <dd>

Questo parametro è diverso da zero se il file è stato reso disponibile offline o 0 in caso contrario.

</dd> <dt>

*lpdwHintFlags* \[ Cambio\]
</dt> <dd>

Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                | Significato                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**FLAG \_ CODICE UTENTE \_ \_ DEL PIN \_**</dt> DEI SUGGERIMENTI CSC <dt>0x01</dt> </dl>                                | Un utente ha reso il file disponibile offline.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**FLAG \_ IL PIN DEL SUGGERIMENTO CSC \_ \_ EREDITA \_ \_ L'0X02**</dt> <dt></dt> </dl>       | Un utente ha reso disponibile l'elemento padre offline e ha contrassegnato l'elemento padre in modo che i relativi elementi figlio siano disponibili offline.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**FLAG \_ IL \_ PIN DELL'HINT CSC \_ EREDITA IL \_ \_ 0X04**</dt> <dt></dt> </dl> | Un amministratore o criteri di gruppo ha reso disponibile l'elemento padre offline e ha contrassegnato l'elemento padre in modo che i relativi elementi figlio siano disponibili offline.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**FLAG \_ SISTEMA \_ DEL \_ \_ PIN HINT CSC**</dt> <dt>0x10</dt> </dl>                          | Un amministratore o criteri di gruppo ha reso il file disponibile offline.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per ricevere le informazioni su data e ora per il file o la sottodirectory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle di ricerca usato in una chiamata successiva a [**CSCFindNextFileW**](cscfindnextfilew.md) o [**CSCFindClose.**](cscfindclose.md)

Se la funzione ha esito negativo, il valore restituito è **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
