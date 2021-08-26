---
description: Annulla la notifica di caricamento dll registrata in precedenza chiamando la funzione LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Funzione LdrUnregisterDllNotification
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
ms.openlocfilehash: c70a732f1e1d1dd71db8d89489066547ee5238e89cf992fca9f2b04759b4c9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001301"
---
# <a name="ldrunregisterdllnotification-function"></a>Funzione LdrUnregisterDllNotification

\[Questa funzione può essere modificata o rimossa da Windows senza preavviso.\]

Annulla la notifica di caricamento dll registrata in precedenza chiamando la [**funzione LdrRegisterDllNotification.**](ldrregisterdllnotification.md)

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cookie* \[ Pollici\]
</dt> <dd>

Puntatore all'identificatore di callback ricevuto dalla chiamata [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) registrata per la notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **CODICE NTSTATUS** o di errore.

Se la funzione ha esito positivo, restituisce **STATUS \_ SUCCESS**.

Se la funzione di callback non viene trovata, la funzione restituisce **STATUS \_ DLL NOT \_ \_ FOUND**.

I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus.h disponibile in WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile in WDK. È anche possibile usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
