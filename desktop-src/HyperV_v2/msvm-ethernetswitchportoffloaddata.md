---
description: Rappresenta i dati sullo stato della funzionalità di offload della porta.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Msvm_EthernetSwitchPortOffloadData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e6e2de8571d665dc86393708b2afcf73fc4885f0b4de26624daafcdccff995b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681481"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a>Classe Msvm \_ EthernetSwitchPortOffloadData

Rappresenta i dati sullo stato della funzionalità di offload della porta.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetSwitchPortOffloadData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetSwitchPortOffloadData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Offload Feature Status".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome della sottoclasse usata nella creazione di questa istanza di dati della porta. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "Msvm \_ EthernetSwitchPortOffloadData".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Rappresenta i dati di stato della funzionalità di offload della porta".

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "Msvm \_ EthernetSwitchPort".

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 64 )
</dt> </dl>

ID dispositivo della porta che ha come ambito questa istanza di dati della porta. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData.**](msvm-ethernetportdata.md)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Offload Feature Status".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IovOffloadUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Utilizzo corrente dell'offload di I/O Virtualization (IOV).

</dd> <dt>

**IovQueuePairUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numero corrente di coppie di code usate dalla porta.

</dd> <dt>

**IovVfDataPathActive**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se il percorso dati VF IOV è attivo.

</dd> <dt>

**IovVfId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificatore VF IOV corrente assegnato alla porta. Questo valore è valido se **IovOffloadUsage** è diverso da zero.

</dd> <dt>

**IpsecCurrentOffloadSaCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numero corrente di slot di offload sa (Security Association) in uso sulla porta.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Stringa che identifica in modo univoco questa istanza di dati della porta nell'ambito del commutatore e della porta. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData.**](msvm-ethernetportdata.md)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** (256)
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "Msvm \_ VirtualEthernetSwitch".

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome del commutatore virtuale che ha come ambito questa istanza di dati della porta. Questa proprietà viene ereditata da [**Msvm \_ EthernetPortData.**](msvm-ethernetportdata.md)

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica se VMMQ è attivo.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica il numero di code usate per VRSS/VMMQ.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**VMQId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificatore della coda della macchina virtuale corrente assegnato alla porta. Questo valore è valido **se VMQOffloadUsage** è diverso da zero.

</dd> <dt>

**VMQOffloadUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Utilizzo dell'offload della coda di macchine virtuali corrente.

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica se vRSS è attivo.

> [!Note]  
> Questa proprietà è stata aggiunta Windows 10 versione 1703.

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica se la CPU VMQ primaria è esclusa dalla tabella di riferimento indiretto VRSS/VMMQ.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica se viene eseguita la distribuzione VRSS/VMMQ sul lato host, indipendentemente dalle impostazioni RSS della scheda di interfaccia di rete virtuale.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica il numero minimo di code usate per VRSS/VMMQ.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica il modo in cui le code VRSS/VMMQ vengono orientate a processori host diversi.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica la modalità di affinità dei canali Vmbus ai processori host.

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



 

