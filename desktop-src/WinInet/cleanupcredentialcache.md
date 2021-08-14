---
title: Funzione CleanupCredentialCache
description: Implementato da alcuni provider di supporto per la sicurezza (SSP) per scaricare la cache delle credenziali del provider di servizi condivisi.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Funzione CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62edb05f401c5ed69092c432f20a7ee96c98afd369e4a4cb0a1acde30e166013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413021"
---
# <a name="cleanupcredentialcache-function"></a>Funzione CleanupCredentialCache

La **funzione CleanupCredentialCache** viene implementata da alcuni provider di supporto per la sicurezza (SSP) per scaricare la cache delle credenziali del provider di servizi condivisi.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

**TRUE** se la funzione ha esito positivo. in caso contrario, **FALSE.**

## <a name="remarks"></a>Commenti

La **funzione CleanupCredentialCache** viene implementata dagli SSP seguenti:

-   MSNSSPC.dll
-   MSAPSSPC.dll

L'implementazione **di CleanupCredentialCache** da parte di questi provider di servizi di configurazione restituisce sempre **TRUE.**

Prima di tentare di ottenere un handle di modulo per esportare **CleanupCredentialCache,** l'applicazione deve verificare che il provider di servizi condivisi caricato sia uno degli SSP noti che implementano la funzione **CleanupCredentialCache.**

Per scaricare la cache delle credenziali del provider di servizi condivisi, l'applicazione deve ottenere un handle di modulo per il provider di servizi condivisi chiamando la [**funzione GetModuleHandle.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) Dopo aver ottenuto il modulo, l'applicazione deve esportare la funzione **CleanupCredentialCache** implementata dal provider di servizi condivisi chiamando la [**funzione GetProcAddress,**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) passando il modulo restituito da **GetModuleHandle** e **CleanupCredentialCache** come parametri di input.

Come tutti gli altri aspetti dell'API WinINet, questa funzione non può essere chiamata in modo sicuro dall'interno di DllMain o dai costruttori e distruttori di oggetti globali.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server usare [Microsoft Windows servizi HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

