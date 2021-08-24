---
description: Rimuove le impostazioni delle funzionalità da una connessione Ethernet della macchina virtuale.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Metodo RemoveFeatureSettings della Msvm_VirtualSystemManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17e87cd7c09b22758ba863d9d591370ae49a5a408e43223970c431bac9f3450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822901"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo RemoveFeatureSettings della classe Msvm \_ VirtualSystemManagementService

Rimuove le impostazioni delle funzionalità da una connessione Ethernet della macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni funzionalità* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**Msvm \_ EthernetSwitchFeatureSettingData,**](msvm-ethernetswitchfeaturesettingdata.md) che definisce le impostazioni di funzionalità da rimuovere. La **proprietà InstanceID** di ognuna di queste istanze identifica le impostazioni di funzionalità da rimuovere.

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

**Stato non valido** (5)
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

 

