---
title: CleanupCredentialCache (funzione)
description: Implementato da determinati provider di supporto per la sicurezza (SSP) per scaricare la cache delle credenziali SSP.
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
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119034"
---
# <a name="cleanupcredentialcache-function"></a>CleanupCredentialCache (funzione)

La funzione **CleanupCredentialCache** viene implementata da determinati provider di supporto della sicurezza (SSP) per scaricare la cache delle credenziali SSP.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

**True** se la funzione ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

La funzione **CleanupCredentialCache** viene implementata dai provider di servizi condivisi seguenti:

-   MSNSSPC.dll
-   MSAPSSPC.dll

L'implementazione di **CleanupCredentialCache** da questi SSP restituisce sempre **true**.

Prima di provare a ottenere un handle del modulo per esportare **CleanupCredentialCache**, l'applicazione deve verificare che il provider di servizi condivisi che è stato caricato sia uno dei SSP noti che implementa la funzione **CleanupCredentialCache** .

Per scaricare la cache delle credenziali SSP, l'applicazione deve ottenere un handle del modulo per il provider di servizi condivisi chiamando la funzione [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) . Dopo aver ottenuto il modulo, l'applicazione deve esportare la funzione **CleanupCredentialCache** implementata dal provider di servizi condivisi chiamando la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , passando il modulo restituito da **GetModuleHandle** e **CleanupCredentialCache** come parametri di input.

Come tutti gli altri aspetti dell'API WinINet, questa funzione non può essere chiamata in modo sicuro da DllMain o dai costruttori e dai distruttori di oggetti globali.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

