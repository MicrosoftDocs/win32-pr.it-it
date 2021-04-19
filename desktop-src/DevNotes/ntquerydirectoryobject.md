---
description: Recupera le informazioni sull'oggetto directory specificato.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject (funzione)
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
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326092"
---
# <a name="ntquerydirectoryobject-function"></a>NtQueryDirectoryObject (funzione)

\[Questa funzione può essere modificata o non disponibile in futuro.\]

Recupera le informazioni sull'oggetto directory specificato.

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

*DirectoryHandle* \[ in\]
</dt> <dd>

Handle per l'oggetto directory.

</dd> <dt>

*Buffer* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve le informazioni sulla directory. Questo buffer riceve una o più strutture di **\_ \_ informazioni di directory degli oggetti** , l'ultima è **null**, seguita da stringhe che contengono i nomi delle voci di directory. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*Lunghezza* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di output fornito dall'utente.

</dd> <dt>

*ReturnSingleEntry* \[ in\]
</dt> <dd>

Indica se la funzione deve restituire solo una singola voce.

</dd> <dt>

*RestartScan* \[ in\]
</dt> <dd>

Indica se riavviare l'analisi o continuare l'enumerazione utilizzando le informazioni passate nel parametro di *contesto* .

</dd> <dt>

*Contesto* \[ in uscita\]
</dt> <dd>

Contesto di enumerazione.

</dd> <dt>

*ReturnLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza delle informazioni di directory restituite nel buffer di output, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.

## <a name="remarks"></a>Commenti

Di seguito è riportata la definizione della struttura delle **\_ \_ informazioni della directory degli oggetti** .

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
