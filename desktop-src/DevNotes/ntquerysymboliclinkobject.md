---
description: Recupera la destinazione di un collegamento simbolico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Funzione NtQuerySymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 805f3de5da380c4749e58dd7467f1f4ccb2471119ffed81b79695a98feb1b090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003631"
---
# <a name="ntquerysymboliclinkobject-function"></a>Funzione NtQuerySymbolicLinkObject

\[Questa funzione potrebbe essere modificata o non disponibile in futuro.\]

Recupera la destinazione di un collegamento simbolico.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LinkHandle* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto collegamento simbolico.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Puntatore a una stringa Unicode inizializzata che riceve la destinazione del collegamento simbolico. I **membri MaximumLength** **e Buffer** devono essere impostati se la chiamata non riesce.

</dd> <dt>

*ReturnedLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza della stringa Unicode restituita nel *parametro LinkTarget.* Se la funzione restituisce **STATUS \_ BUFFER TOO \_ \_ SMALL,** questa variabile riceve le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **STATUS \_ SUCCESS o** uno stato di errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
