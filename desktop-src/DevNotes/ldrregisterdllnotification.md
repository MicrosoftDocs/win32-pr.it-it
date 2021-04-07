---
description: Esegue la registrazione per la notifica quando una DLL viene caricata per la prima volta. Questa notifica si verifica prima che venga eseguito il collegamento dinamico.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049101"
---
# <a name="ldrregisterdllnotification-function"></a>LdrRegisterDllNotification (funzione)

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]

Esegue la registrazione per la notifica quando una DLL viene caricata per la prima volta. Questa notifica si verifica prima che venga eseguito il collegamento dinamico.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Questo parametro deve essere zero.

</dd> <dt>

*NotificationFunction* \[ in\]
</dt> <dd>

Puntatore a una funzione di callback di notifica [*LdrDllNotification*](ldrdllnotification.md) da chiamare quando la dll viene caricata.

</dd> <dt>

*Contesto* \[ in, facoltativo\]
</dt> <dd>

Puntatore ai dati di contesto per la funzione di callback.

</dd> <dt>

*Cookie* \[ out\]
</dt> <dd>

Puntatore a una variabile per ricevere un identificatore per la funzione di callback. Questo identificatore viene utilizzato per annullare la registrazione della funzione di callback di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.

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

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
