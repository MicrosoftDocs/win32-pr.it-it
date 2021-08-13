---
title: Funzione DDCCIGetVCPFeature
description: Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice vcp (Virtual Pannello di controllo) per un monitoraggio.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640999"
---
# <a name="ddccigetvcpfeature-function"></a>Funzione DDCCIGetVCPFeature

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice vcp (Virtual Pannello di controllo) per un monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ Pollici\]
</dt> <dd>

Handle per un monitoraggio fisico.

</dd> <dt>

*dwVCPCode* \[ Pollici\]
</dt> <dd>

Codice VCP su cui eseguire una query.

</dd> <dt>

*pvct* \[ out, facoltativo\]
</dt> <dd>

Riceve il tipo di codice VCP come membro [**dell'enumerazione MC \_ VCP CODE \_ \_ TYPE.**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type)

</dd> <dt>

*pdwCurrentValue* \[ Cambio\]
</dt> <dd>

Riceve il valore corrente del codice VCP.

</dd> <dt>

*pdwMaximumValue* \[ out, facoltativo\]
</dt> <dd>

Riceve il valore massimo del codice VCP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Le applicazioni devono [**chiamare GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) anziché questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

