---
description: Aggiunge risorse a una configurazione di macchina virtuale.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Metodo AddResourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0092b19a0fa4bf41492c42db0b3346607bd3b587a2e57e789815424d94a89850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900471"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddResourceSettings della classe Msvm \_ VirtualSystemManagementService

Aggiunge risorse a una configurazione di macchina virtuale. Se applicato a una configurazione di macchina virtuale "state", come effetto collaterale, le risorse vengono aggiunte alla macchina virtuale attiva.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedConfiguration* \[ Pollici\]
</dt> <dd>

Riferimento a un oggetto [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che rappresenta la configurazione della macchina virtuale interessata.

</dd> <dt>

*ResourceSettings* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere alla macchina virtuale.

</dd> <dt>

*ResultingResourceSettings* \[ Cambio\]
</dt> <dd>

Matrice di riferimenti a istanze della [**classe CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresenta gli aspetti virtuali delle risorse virtuali aggiunte.

</dd> <dt>

*Processo* \[ Cambio\]
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

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
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
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

