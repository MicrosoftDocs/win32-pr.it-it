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
ms.openlocfilehash: ea13050c2c8e52d5786a97b3b749f10e48a73c4ecf1274e0415967ad25c9d9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521481"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Metodo ControlSampleTimes della classe Msvm \_ MetricService

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

*StartSampleTime* \[ Pollici\]
</dt> <dd>

Momento in cui deve essere avviato il campionamento per le metriche.

Il valore 99990101000000.000000+000 indica che il campionamento deve iniziare alla successiva sincronizzazione con l'ora intera. Il campionamento viene sincronizzato con l'ora intera se i secondi dall'intervallo di campionamento modulo di mezzanotte in secondi è uguale a 0.

</dd> <dt>

*PreferredSampleInterval* \[ Pollici\]
</dt> <dd>

Intervallo di campionamento preferito. Per ottenere le metriche correlatabili, è consigliabile scegliere l'intervallo di campionamento in modo che l'intervallo di campionamento di 3600 modulo in secondi sia uguale a 0.

È responsabilità dell'implementazione del servizio metrica CIM decidere se il tempo richiesto per l'intervallo di campionamento viene rispettato.

Il client CIM può controllare se i provider di metriche rispettano il tempo di intervallo di campionamento richiesto recuperando le istanze di BaseMetricDefinition correlate e controllando il contenuto della proprietà "CIM \_ BaseMetricDefinition.SampleInterval".

</dd> <dt>

*RestartGathering* \[ Pollici\]
</dt> <dd>

Valore booleano che, se impostato su TRUE, richiede che la raccolta di tutte le metriche associate al servizio metrica sia ri avviata con questa chiamata al metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Metodo riservato** (..)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




