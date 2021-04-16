---
description: Rappresenta lo stato configurato del dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527667"
---
# <a name="msvm_tpmsettingdata-class"></a>\_Classe MSVM TPMSettingData

Rappresenta lo stato configurato del dispositivo TPM.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Members

La **classe \_ TPMSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TPMSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**Dataprotected**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per impostare un criterio per proteggere i dati di una macchina virtuale. in caso contrario, **false**. Un TPM appena creato è disabilitato, quindi lo stato di protezione dati iniziale è **false**.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Il valore predefinito è **disabled**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Protector**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

La protezione con chiave dal client del servizio sorveglianza host.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

L'ultima protezione con chiave valida nota ha crittografato correttamente lo stato del dispositivo TPM nell'ultimo avvio della macchina virtuale.

Questa proprietà è di sola lettura per il client WMI e può essere modificata solo dal dispositivo TPM della macchina virtuale.

</dd> <dt>

**Schermato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per definire un criterio per la schermatura di una macchina virtuale. in caso contrario, **false**. Un TPM appena creato è disabilitato, quindi lo stato di schermatura iniziale è **false**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                                   |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

