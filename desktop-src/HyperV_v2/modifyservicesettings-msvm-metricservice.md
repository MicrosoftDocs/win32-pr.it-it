---
description: Modifica i dati dell'impostazione per il servizio.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Metodo ModifyServiceSettings della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752223"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Metodo ModifyServiceSettings della classe MSVM \_ MetricService

Modifica i dati dell'impostazione per il servizio.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SettingData* \[ in\]
</dt> <dd>

Contiene un'istanza incorporata della [**classe \_ MetricServiceSettingData di MSVM**](msvm-metricservicesettingdata.md) che contiene i dati di impostazione modificati per il servizio.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                    | Esito positivo.<br/>                                |
| <dl> <dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt> </dl> | Parametri del metodo controllati, processo avviato.<br/> |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                 | non riuscito.<br/>                                 |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                          | Accesso negato.<br/>                          |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                          | Non supportata.<br/>                          |
| <dl> <dt>**Stato sconosciuto**</dt> <dt>32771</dt> </dl>                      | Lo stato è sconosciuto.<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout.<br/>                               |
| <dl> <dt>**Parametro non valido**</dt> <dt>32773</dt> </dl>                      | Parametro non valido.<br/>                      |
| <dl> Il <dt>**sistema è in uso**</dt> <dt>32774</dt> </dl>                       | Il sistema è in uso.<br/>                       |
| <dl> <dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt> </dl>       | Stato non valido per questa operazione.<br/>       |
| <dl> <dt>**Tipo di dati non corretto**</dt> <dt>32776</dt> </dl>                    | Tipo di dati non corretto.<br/>                    |
| <dl> Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt> </dl>                | Il sistema non è disponibile.<br/>                |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                          | Memoria insufficiente.<br/>                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MetricService MSVM**](msvm-metricservice.md)
</dt> </dl>

 

