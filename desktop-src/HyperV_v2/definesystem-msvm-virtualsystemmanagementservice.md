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
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232691"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo DefineSystem della classe MSVM \_ VirtualSystemManagementService

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

*SystemSettings* \[ in\]
</dt> <dd>

Tipo: **stringa**

Istanza incorporata della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) utilizzata per definire gli attributi della macchina virtuale da creare. Questo parametro è obbligatorio.

</dd> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Tipo: **stringa \[ \]**

Numero di istanze incorporate della classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (o delle relative classi derivate). Insieme, queste istanze descrivono le risorse virtuali della macchina virtuale. Verrà creato un set predefinito di dispositivi per la macchina virtuale, indipendentemente dal fatto che questo parametro sia impostato. Il processore e la memoria, ad esempio, vengono creati e configurati automaticamente con i valori predefiniti.

</dd> <dt>

*ReferenceConfiguration* \[ in\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione di macchina virtuale di riferimento. La configurazione di riferimento viene usata per completare la configurazione della nuova macchina virtuale se i parametri *SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale appena creata.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo. Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del *processo* può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona. Qualsiasi altro valore restituito indica un errore.

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

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

 

