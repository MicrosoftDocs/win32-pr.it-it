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
ms.openlocfilehash: a18145a2b59e1ba93967ad7f1d529466dfc1e6ac094b74d139a36fbe6f77a57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068641"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Metodo DefineSystem della classe CIM \_ VirtualSystemManagementService

Definisce un sistema virtuale.

L'input non completamente specificato può essere compilato con valori predefiniti.

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

*SystemSettings* \[ Pollici\]
</dt> <dd>

Stringa contenente un'istanza incorporata della [**classe CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) usata per definire gli attributi del sistema virtuale da creare.

</dd> <dt>

*ResourceSettings* \[ Pollici\]
</dt> <dd>

Matrice di stringhe ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive gli aspetti virtuali di una risorsa virtuale da creare nell'ambito del nuovo sistema virtuale.

</dd> <dt>

*ReferenceConfiguration* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza dell'oggetto CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione del sistema virtuale di riferimento. La configurazione di riferimento viene usata per integrare la configurazione del nuovo sistema virtuale se i *parametri SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.

</dd> <dt>

*ResultingSystem* \[ Cambio\]
</dt> <dd>

Se un sistema di computer virtuale viene definito correttamente, viene restituito un riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale appena definito.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un processo. In questo caso, l'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il nuovo sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) alla proprietà **AffectedElement che** fa riferimento alla nuova istanza della classe **CIM \_ ComputerSystem** e alla proprietà **ElementEffects** impostata su 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




