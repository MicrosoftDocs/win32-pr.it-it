---
description: Aggiunge le impostazioni delle funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.
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
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345561"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddFeatureSettings della classe MSVM \_ VirtualSystemManagementService

Aggiunge le impostazioni delle funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.

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

*AffectedConfiguration* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la connessione Ethernet interessata.

</dd> <dt>

*FeatureSettings* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md) che descrive le impostazioni della funzionalità da aggiungere alla configurazione della connessione.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Matrice di riferimenti a istanze della classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni della funzionalità aggiunte.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

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

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

