---
description: Imposta i tempi di campionamento del controllo.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Metodo ControlSampleTimes della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227420"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Metodo ControlSampleTimes della classe MSVM \_ MetricService

Imposta i tempi di campionamento del controllo.

## <a name="syntax"></a>Sintassi


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartSampleTime* \[ in\]
</dt> <dd>

Temporizzazione per l'avvio del campionamento per le metriche.

Il valore 99990101000000.000000 + 000 indicherà che il campionamento deve iniziare alla successiva sincronizzazione con l'ora completa. Il campionamento viene sincronizzato con l'ora intera se i secondi dall'intervallo di campionamento del modulo mezzanotte in secondi è uguale a 0.

</dd> <dt>

*PreferredSampleInterval* \[ in\]
</dt> <dd>

Tempo di intervallo di campionamento preferito. Per ottenere metriche correlate, è consigliabile scegliere l'intervallo di campionamento in modo che l'intervallo di campionamento di esempio di 3600 modulo in secondi sia uguale a 0.

È responsabilità dell'implementazione del servizio metrica CIM decidere se il tempo richiesto per l'intervallo di campionamento viene rispettato.

Il client CIM può verificare se i provider di metriche rispettano il tempo di intervallo di campionamento richiesto recuperando le istanze di BaseMetricDefinition correlate e controllando il contenuto della \_ Proprietà "CIM BaseMetricDefinition. SampleInterval".

</dd> <dt>

*RestartGathering* \[ in\]
</dt> <dd>

Valore booleano che, se impostato su TRUE, richiede che la raccolta di tutte le metriche associate al servizio della metrica venga riavviata con questa chiamata al metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Metodo riservato** (..)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MetricService MSVM**](msvm-metricservice.md)
</dt> </dl>

 

 




