---
title: DDCCIGetTimingReport (funzione)
description: Ottiene le frequenze di sincronizzazione orizzontali e verticali di un monitoraggio.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964193"
---
# <a name="ddccigettimingreport-function"></a>DDCCIGetTimingReport (funzione)

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene le frequenze di sincronizzazione orizzontali e verticali di un monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ in\]
</dt> <dd>

Handle per un monitor fisico.

</dd> <dt>

*PMTR* \[ out\]
</dt> <dd>

Un puntatore a una struttura del [**\_ \_ report temporizzato MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) che riceve le informazioni sull'intervallo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) invece di chiamare questa funzione.

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

 

