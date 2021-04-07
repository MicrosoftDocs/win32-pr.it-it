---
title: DDCCIGetVCPFeature (funzione)
description: Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.
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
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964192"
---
# <a name="ddccigetvcpfeature-function"></a>DDCCIGetVCPFeature (funzione)

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.

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

*hMonitor* \[ in\]
</dt> <dd>

Handle per un monitor fisico.

</dd> <dt>

*dwVCPCode* \[ in\]
</dt> <dd>

Codice VCP per la query.

</dd> <dt>

*pvct* \[ out, facoltativo\]
</dt> <dd>

Riceve il tipo di codice VCP come membro dell'enumerazione del [**\_ tipo di \_ codice \_ MC VCP**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .

</dd> <dt>

*pdwCurrentValue* \[ out\]
</dt> <dd>

Riceve il valore corrente del codice VCP.

</dd> <dt>

*pdwMaximumValue* \[ out, facoltativo\]
</dt> <dd>

Riceve il valore massimo del codice VCP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) invece di chiamare questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

