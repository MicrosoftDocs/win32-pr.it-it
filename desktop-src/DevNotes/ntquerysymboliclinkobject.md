---
description: Recupera la destinazione di un collegamento simbolico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject (funzione)
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
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326088"
---
# <a name="ntquerysymboliclinkobject-function"></a>NtQuerySymbolicLinkObject (funzione)

\[Questa funzione può essere modificata o non disponibile in futuro.\]

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

*LinkHandle* \[ in\]
</dt> <dd>

Handle per l'oggetto di collegamento simbolico.

</dd> <dt>

*LinkTarget* \[ in uscita\]
</dt> <dd>

Puntatore a una stringa Unicode inizializzata che riceve la destinazione del collegamento simbolico. Se la chiamata ha esito negativo, è necessario impostare i membri **MaximumLength** e **buffer** .

</dd> <dt>

*ReturnedLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza della stringa Unicode restituita nel parametro *LinkTarget* . Se la funzione restituisce **un \_ buffer di stato \_ troppo \_ piccolo**, questa variabile riceve le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
