---
description: Rimuove le impostazioni delle risorse virtuali da una configurazione di macchina virtuale.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Metodo RemoveResourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307866"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo RemoveResourceSettings della classe MSVM \_ VirtualSystemManagementService

Rimuove le impostazioni delle risorse virtuali da una configurazione di macchina virtuale. Quando applicato alle parti di una configurazione della macchina virtuale corrente, la macchina virtuale attiva può essere rimossa.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , in cui ogni istanza rappresenta le impostazioni di una risorsa virtuale all'interno di una configurazione di macchina virtuale da rimuovere.

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

**Stato non valido** (5)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**DMTF riservato** (..)
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

 

