---
description: Cerca un file nella cache File offline che soddisfi i criteri specificati.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW (funzione)
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
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331198"
---
# <a name="cscfindfirstfilew-function"></a>CSCFindFirstFileW (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

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

*lpszFileName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica una directory o un percorso UNC valido.

</dd> <dt>

*lpFind32* \[ out\]
</dt> <dd>

Puntatore alla struttura di [**\_ \_ dati Find Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) che riceve informazioni sul file o sulla sottodirectory.

</dd> <dt>

*lpdwStatus* \[ out\]
</dt> <dd>

Codice NTSTATUS che indica lo stato della chiamata.

</dd> <dt>

*lpdwPinCount* \[ out\]
</dt> <dd>

Questo parametro è diverso da zero se il file è stato reso disponibile offline o 0 in caso contrario.

</dd> <dt>

*lpdwHintFlags* \[ out\]
</dt> <dd>

Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                | Significato                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Flag \_ di 0x01 \_ \_ \_ utente pin hint CSC**</dt> <dt></dt> </dl>                                | Un utente ha reso disponibile il file offline.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Flag \_ di Il \_ \_ pin dell'hint CSC \_ eredita l' \_ utente**</dt> <dt>0x02</dt> </dl>       | Un utente ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Flag \_ di Il \_ pin dell'hint CSC \_ eredita il \_ \_ sistema**</dt> <dt>0x04</dt> </dl> | Un amministratore o un criterio di gruppo ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Flag \_ di 0x10 \_ \_ \_ sistema pin hint CSC**</dt> <dt></dt> </dl>                          | Un amministratore o un criterio di gruppo ha reso disponibile il file offline.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ out\]
</dt> <dd>

Puntatore a una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per ricevere le informazioni sulla data e l'ora per il file o la sottodirectory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle di ricerca usato in una chiamata successiva a [**CSCFindNextFileW**](cscfindnextfilew.md) o [**CSCFindClose**](cscfindclose.md).

Se la funzione ha esito negativo, il valore restituito è **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
