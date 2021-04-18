---
description: Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Metodo IVmApplicationHealthMonitor:: SetApplicationState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309506"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>Metodo IVmApplicationHealthMonitor:: SetApplicationState

Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Rappresentazione **BSTR** del **GUID** che identifica l'applicazione. È responsabilità dell'applicazione chiamante creare e gestire gli identificatori usati per le applicazioni monitorate.

</dd> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome visualizzato dell'applicazione. Questo nome viene utilizzato in una voce del registro eventi informativa per la modifica dello stato.

</dd> <dt>

*Stato* \[ di in\]
</dt> <dd>

Valore dell'enumerazione [**\_ dello stato dell'applicazione**](application-state.md) che specifica il nuovo stato di integrità dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel  \[ \] valore della proprietà OperationalStatus 1 della classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .

Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                      |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




