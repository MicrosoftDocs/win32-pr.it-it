---
description: Recupera informazioni sull'oggetto directory specificato.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Funzione NtQueryDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 11c7240cf63fa2f7e13338a0e0459e172e41aa1ed71db90c661b8aad0915d670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079671"
---
# <a name="ntquerydirectoryobject-function"></a>Funzione NtQueryDirectoryObject

\[Questa funzione potrebbe essere modificata o non disponibile in futuro.\]

Recupera informazioni sull'oggetto directory specificato.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryHandle* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto directory.

</dd> <dt>

*Buffer* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve le informazioni sulla directory. Questo buffer riceve una o più strutture **OBJECT \_ DIRECTORY \_ INFORMATION,** l'ultima è **NULL,** seguita da stringhe che contengono i nomi delle voci di directory. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*Lunghezza* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer di output fornito dall'utente, in byte.

</dd> <dt>

*ReturnSingleEntry* \[ Pollici\]
</dt> <dd>

Indica se la funzione deve restituire una sola voce.

</dd> <dt>

*RestartScan* \[ Pollici\]
</dt> <dd>

Indica se riavviare l'analisi o continuare l'enumerazione utilizzando le informazioni passate nel *parametro Context.*

</dd> <dt>

*Contesto* \[ in, out\]
</dt> <dd>

Contesto di enumerazione.

</dd> <dt>

*ReturnLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza in byte delle informazioni sulla directory restituite nel buffer di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **STATUS \_ SUCCESS o** uno stato di errore.

## <a name="remarks"></a>Commenti

Di seguito è riportata la definizione della **struttura OBJECT \_ DIRECTORY \_ INFORMATION.**

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
