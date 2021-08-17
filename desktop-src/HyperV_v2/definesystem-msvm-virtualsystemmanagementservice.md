---
description: Crea una nuova istanza di macchina virtuale.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Metodo DefineSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47b01a2fb0935873b5a36d69376eb09bfe6d4555613c0eb8dc8907589d4f5f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645812"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo DefineSystem della classe Msvm \_ VirtualSystemManagementService

Crea una nuova istanza di macchina virtuale. Le proprietà non specificate verranno popolate con i valori predefiniti.

## <a name="syntax"></a>Sintassi


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni di sistema* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Istanza incorporata della [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) usata per definire gli attributi della macchina virtuale da creare. Questo parametro è obbligatorio.

</dd> <dt>

*ResourceSettings* \[ Pollici\]
</dt> <dd>

Tipo: **\[ \] string**

Numero di istanze incorporate della [**classe Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (o delle classi derivate). Insieme, queste istanze descrivono le risorse virtuali della macchina virtuale. Verrà creato un set predefinito di dispositivi per la macchina virtuale, indipendentemente dal fatto che questo parametro sia impostato. Ad esempio, il processore e la memoria vengono creati e configurati automaticamente con i valori predefiniti.

</dd> <dt>

*ReferenceConfiguration* \[ Pollici\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Riferimento a un'istanza della [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione di macchina virtuale di riferimento. La configurazione di riferimento viene usata per integrare la configurazione della nuova macchina virtuale se i parametri *SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.

</dd> <dt>

*ResultingSystem* \[ Cambio\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Riferimento a un'istanza della [**classe \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale appena creata.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo. Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output *Job* può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona. Qualsiasi altro valore restituito indica un errore.

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

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

 

