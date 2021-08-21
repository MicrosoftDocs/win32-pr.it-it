---
description: Rappresenta i dati dell'impostazione della funzionalità di offload delle porte.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddf58a10e85003a00e0d757f29db55a49f98f0ba22e8c3124b83a593f2a3908f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148300"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortOffloadSettingData

Rappresenta i dati dell'impostazione della funzionalità di offload delle porte.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetSwitchPortOffloadSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetSwitchPortOffloadSettingData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Offload Impostazioni".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Rappresenta i dati delle impostazioni della funzionalità di offload delle porte".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Offload Impostazioni".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IOVInterruptModeration**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore di moderazione interrupt per l'offload I/O Virtualization (IOV). Il valore predefinito è 0.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (0)


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

**Adattivo** (1)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Disattivato** (2)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Bassa** (100)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Media** (200)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Alta** (300)


</dt> <dd></dd> </dl>

</dd> <dt>

**IOVOffloadWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Peso assegnato a questa porta per l'offload I/O Virtualization (IOV). Il peso è l'importanza relativa durante l'assegnazione delle risorse IOV. **L'impostazione della proprietà IOVOffloadWeight** su 0 disabilita l'offload IOV sulla porta. Il valore predefinito è 0.

</dd> <dt>

**IOVQueuePairsRequested**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numero di coppie di code richieste per questa porta per l'offload I/O Virtualization (IOV). Il valore predefinito è 1.

</dd> <dt>

**IPSecOffloadLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numero massimo di slot di offload dell'associazione di sicurezza consentiti dalla porta.

</dd> <dt>

**PacketDirectModerationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Valore del conteggio della moderazione di interrupt per Packet Direct (PD). Il valore predefinito è 0.

> [!Note]  
> Proprietà aggiunta in Windows 10.

 

</dd> <dt>

**PacketDirectModerationInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Valore dell'intervallo di moderazione di interrupt per Packet Direct (PD). Il valore predefinito è 0.

> [!Note]  
> Proprietà aggiunta in Windows 10.

 

</dd> <dt>

**PacketDirectNumProcs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Numero di processori utilizzati dall'host per l'elaborazione dei pacchetti inviati da questa porta in modalità diretta pacchetti. Il valore predefinito è 1.

> [!Note]  
> Proprietà aggiunta in Windows 10.

 

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Abilitare l'offload VMMQ se supportato dall'hardware. Il valore predefinito è False.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Numero di code da allocare quando VRSS è abilitato. Il valore predefinito è 16.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**VMQOffloadWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Peso assegnato a questa porta per l'offload della coda di macchine virtuali. Il peso è l'importanza relativa durante l'assegnazione delle risorse vmq. **L'impostazione della proprietà VMQOffloadWeight** su 0 disabilita VMQ sulla porta. Il valore predefinito è 100.

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Abilitare VRSS. Il valore predefinito è true.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Se escludere il processore VMQ primario dalla tabella di riferimento indiretto VRSS quando VRSS è abilitato. Il valore predefinito è false.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indica se eseguire sempre vrSS sul lato host quando è abilitato VRSS, indipendentemente dall'impostazione RSS della scheda di interfaccia di rete virtuale. Il valore predefinito è false.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Numero minimo di code da allocare quando VRSS è abilitato. Il valore predefinito è 1.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Modalità di pianificazione delle code da usare quando vrSS è abilitato. Il valore predefinito è la pianificazione statica.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Criteri di affinità del canale vmbus da usare quando VRSS è abilitato. Il valore predefinito è strong.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

