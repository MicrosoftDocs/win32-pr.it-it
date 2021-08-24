---
description: "Metodo ModifyServiceSettings della classe Msvm_MetricService: modifica i dati dell'impostazione per il servizio."
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
ms.openlocfilehash: 51af98d230433687d9a16cb3ab858fd746b7ff1ca4e17eaf0b36cce16e92c875
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693911"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Metodo ModifyServiceSettings della classe Msvm \_ MetricService

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

*Impostazione dei dati* \[ Pollici\]
</dt> <dd>

Contiene un'istanza incorporata della [**classe Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) che contiene i dati delle impostazioni modificate per il servizio.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>                    | Operazione completata.<br/>                                |
| <dl> <dt>**Parametri del metodo verificati - Processo avviato**</dt> <dt>4096</dt> </dl> | Parametri del metodo controllati, processo avviato.<br/> |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                 | non riuscito.<br/>                                 |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                          | Accesso negato.<br/>                          |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                          | Non supportata.<br/>                          |
| <dl> <dt>**Lo stato è sconosciuto**</dt> <dt>32771</dt> </dl>                      | Lo stato è sconosciuto.<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout.<br/>                               |
| <dl> <dt>**Parametro**</dt> <dt>32773 non valido</dt> </dl>                      | Parametro non valido.<br/>                      |
| <dl> <dt>**Il sistema è in uso**</dt> <dt>32774</dt> </dl>                       | Il sistema è in uso.<br/>                       |
| <dl> <dt>**Stato non valido per questa operazione**</dt> <dt>32775</dt> </dl>       | Stato non valido per questa operazione.<br/>       |
| <dl> <dt>**Tipo di dati**</dt> <dt>32776 non corretto</dt> </dl>                    | Tipo di dati non corretto.<br/>                    |
| <dl> <dt>**Il sistema non è disponibile**</dt> <dt>32777</dt> </dl>                | Il sistema non è disponibile.<br/>                |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                          | Memoria insufficiente.<br/>                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

