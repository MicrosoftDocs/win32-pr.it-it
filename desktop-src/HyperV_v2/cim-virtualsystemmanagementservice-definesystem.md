---
description: Definisce un sistema virtuale.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Metodo DefineSystem della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310552"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Metodo DefineSystem della classe CIM \_ VirtualSystemManagementService

Definisce un sistema virtuale.

L'input non completamente specificato può essere compilato con i valori predefiniti.

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

Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) utilizzata per definire gli attributi del sistema virtuale da creare.

</dd> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive gli aspetti virtuali di una risorsa virtuale da creare nell'ambito del nuovo sistema virtuale.

</dd> <dt>

*ReferenceConfiguration* \[ in\]
</dt> <dd>

Riferimento a un'istanza di oggetto [**\_ VirtualSystemSettingDat CIM**](cim-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione di sistema virtuale di riferimento. La configurazione di riferimento viene utilizzata per completare la configurazione del nuovo sistema virtuale se i parametri *SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Se un sistema di computer virtuale viene definito correttamente, viene restituito un riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale appena definito.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo. In questo caso, l'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il nuovo sistema virtuale viene presentata tramite [**Association CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con la proprietà **interessata** che fa riferimento alla nuova istanza della classe **CIM \_ ComputerSystem** e la proprietà **ElementEffects** impostata su 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




