---
description: Consente di specificare l'avvio della raccolta delle metriche temporiche e di specificare l'intervallo di campionamento preferito per la raccolta dati periodica.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Metodo ControlSampleTimes della CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 833e828a7622dfcd76a7b061e3890fbe111de10a6b8c3c2d3faf0801429678f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695071"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>Metodo ControlSampleTimes della classe \_ CIM MetricService

Consente di specificare l'avvio della raccolta delle metriche temporiche e di specificare l'intervallo di campionamento preferito per la raccolta dati periodica.

Ogni volta che viene avviato il campionamento per metriche aggiuntive, è possibile usare le impostazioni specificate da questo metodo.

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

Il client CIM può verificare se i provider di metriche rispettano il tempo di intervallo di campionamento richiesto recuperando le istanze di BaseMetricDefinition correlate e controllando il contenuto di [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md)**Proprietà SampleInterval.**

</dd> <dt>

*RestartGathering* \[ Pollici\]
</dt> <dd>

**TRUE** per richiedere che la raccolta di tutte le metriche associate al servizio metrica sia avviata di nuovo con questa chiamata al metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




