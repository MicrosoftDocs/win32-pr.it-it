---
description: Descrive le funzionalità e la gestione di un controller seriale.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: CIM_SerialController classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6a438919674f805f59cb6e2cac6e76cb6367f03ce12fa2ceb0787527e56adb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980831"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a>CIM_SerialController classe (gestione Hyper-V)

Descrive le funzionalità e la gestione di un controller seriale.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a>Members

La **classe CIM \_ SerialController** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ SerialController** ha queste proprietà.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Porte seriali DMTF \| \| 004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")
</dt> </dl>

Compatibilità a livello di chip per il controller seriale. Questa proprietà descrive il buffering e altre funzionalità del controller seriale che potrebbero essere intrinseche nell'hardware del chip.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

**Compatibile con XT/AT** (3)


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

**16450 compatibile** (4)


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

**16550 compatibile** (5)


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

**16550A compatibile** (6)


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**8251 Compatibile** (160)


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

**Compatibile con 8251FIFO** (161)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Funzionalità**")
</dt> </dl>

Matrice che contiene spiegazioni più dettagliate per le funzionalità del controller seriale nella matrice **Capabilities.** Gli elementi nella **matrice CapabilityDescriptions** sono correlati a quelli nella **matrice Capabilities.**

</dd> <dt>

**MaxBaudRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Porte seriali DMTF \| \| 004.6"), **PUnit** ("bit/secondo")
</dt> </dl>

Velocità massima in baud in bit al secondo supportata dal controller seriale.

</dd> <dt>

**Sicurezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Porte seriali DMTF \| \| 004.9")
</dt> </dl>

Sicurezza operativa per il controller.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (3)


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**Interfaccia esterna bloccata** (4)


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**Interfaccia esterna abilitata** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Bypass di** avvio (6)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ Controller**](cim-controller.md)
</dt> </dl>

 

