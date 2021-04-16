---
description: Annulla la notifica di caricamento DLL precedentemente registrata chiamando la funzione LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401360"
---
# <a name="ldrunregisterdllnotification-function"></a>LdrUnregisterDllNotification (funzione)

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]

Annulla la notifica di caricamento DLL precedentemente registrata chiamando la funzione [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cookie* \[ in\]
</dt> <dd>

Puntatore all'identificatore di callback ricevuto dalla chiamata [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) registrata per la notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice **NTSTATUS** o Error.

Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.

Se la funzione di callback non viene trovata, la funzione restituisce la **dll di stato \_ \_ non \_ trovata**.

I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll. lib, è disponibile in WDK. È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
