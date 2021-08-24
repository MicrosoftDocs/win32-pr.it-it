---
description: Aggiunge le impostazioni della funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Metodo AddFeatureSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d81fb7dd8f7b4c9d3259977c6cdaf1498490c3617699f1d19ccdb47e5eb6b34d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746551"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddFeatureSettings della classe Msvm \_ VirtualSystemManagementService

Aggiunge le impostazioni della funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedConfiguration* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della [**classe Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la connessione Ethernet interessata.

</dd> <dt>

*Impostazioni funzionalità* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) che descrive le impostazioni delle funzionalità da aggiungere alla configurazione della connessione.

</dd> <dt>

*ResultingFeatureSettings* \[ Cambio\]
</dt> <dd>

Matrice di riferimenti a istanze della [**classe Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni di funzionalità aggiunte.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

