---
title: Funzione DDCCISetVCPFeature
description: Imposta il valore di un codice VCP (Virtual Pannello di controllo) per un monitoraggio.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configurazione del monitoraggio della funzione DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecbfb6172ffd61dd7882895c0db15baddf28986493b202e2fd873135cee41d76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806149"
---
# <a name="ddccisetvcpfeature-function"></a>Funzione DDCCISetVCPFeature

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Imposta il valore di un codice VCP (Virtual Pannello di controllo) per un monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ Pollici\]
</dt> <dd>

Handle per un monitor fisico.

</dd> <dt>

*dwVCPCode* \[ Pollici\]
</dt> <dd>

Codice VCP da impostare.

</dd> <dt>

*dwNewValue* \[ Pollici\]
</dt> <dd>

Valore del codice VCP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Le applicazioni devono [**chiamare SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) anziché questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

