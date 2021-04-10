---
description: Rappresenta una relazione tra un controller e un dispositivo logico gestito dal controller.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Classe CIM_ControlledBy (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879770"
---
# <a name="cim_controlledby-class-hyper-v-management"></a>Classe CIM_ControlledBy (gestione Hyper-V)

Rappresenta una relazione tra un controller e un dispositivo logico gestito dal controller.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ControlledBy** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ControlledBy** dispone di queste proprietà.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà che descrive l'accessibilità del dispositivo tramite il controller.

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

**ReadWrite** (2)


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

**ReadOnly** (3)


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

**NoAccess** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità per l'accesso del dispositivo tramite il controller. Un valore inferiore indica una priorità più alta.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta gestendo attivamente il dispositivo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Attivo** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inattivo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ controller CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Controller.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Dispositivi logici.

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo associato nel contesto del controller.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **contatore**
</dt> </dl>

Numero di reimpostazioni rigide rilasciate dal controller. Una reimpostazione hardware restituisce un dispositivo alla relativa inizializzazione o allo stato di avvio, dopo il quale vengono perse tutte le informazioni e i dati sullo stato dei dispositivi interni.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **contatore**
</dt> </dl>

Numero di reimpostazioni Soft emesse dal controller. Un ripristino soft non cancella lo stato o i dati del dispositivo.

</dd> <dt>

**TimeOfDeviceReset (ora**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora dell'ultima reimpostazione del dispositivo downstream da parte del controller.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DEVICECONNECTION CIM**](cim-deviceconnection.md)
</dt> </dl>

 

