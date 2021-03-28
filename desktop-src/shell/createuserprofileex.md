---
description: Crea un profilo utente per un utente specificato.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982947"
---
# <a name="createuserprofileex-function"></a>CreateUserProfileEx (funzione)

\[Questa funzione non è disponibile a partire da Windows Vista.\]

Crea un profilo utente per un utente specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PSID* \[ in\]
</dt> <dd>

Tipo: **PSID**

SID del nuovo utente.

</dd> <dt>

*lpUsername* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a un buffer contenente il nome utente del nuovo utente.

</dd> <dt>

*lpUserHive* \[ in, facoltativo\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a un buffer che contiene l' [hive del registro di sistema](../sysinfo/registry-hives.md) da usare. Questo parametro può essere **NULL**.

</dd> <dt>

*lpProfileDir* \[ out, facoltativo\]
</dt> <dd>

Tipo: **LPTSTR**

Puntatore a un buffer che, quando questa funzione restituisce, riceve il percorso della directory del profilo dell'utente. Questo parametro può essere **NULL**.

</dd> <dt>

*dwDirSize* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Dimensioni del buffer specificato da *lpProfileDir*, in TCHARs.

</dd> <dt>

*bWin9xUpg* \[ in\]
</dt> <dd>

Tipo: **bool**

**True** se il profilo utente viene creato come parte della migrazione di un profilo da Windows 9x; in caso contrario, **false**.

Se è **true**, il profilo utente viene configurato nella directory predefinita del profilo, in genere C: \\ Documents and Settings \\ *username*. Se la directory esiste già, viene utilizzata. In caso contrario, viene creato.

Se **false**, la directory predefinita del profilo viene creata se non esiste. Se la directory predefinita del profilo esiste già, per questo profilo utente viene creata una nuova directory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce **true** se il nuovo profilo utente è stato creato correttamente; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questa funzione non è dichiarata nelle intestazioni Software Development Kit (SDK) e non dispone di librerie di importazione associate. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento a Userenv.dll. Viene fatto riferimento alla versione ANSI della funzione **CreateUserProfileExA** da Userenv.dll come ordinale 153. Per la versione Unicode viene fatto riferimento a **CreateUserProfileExW** come ordinale 154.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/>  | Windows XP<br/>                                                                  |
| DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/> | **CreateUserProfileExW** (Unicode) e **CreateUserProfileExA** (ANSI)<br/>      |



 

 
