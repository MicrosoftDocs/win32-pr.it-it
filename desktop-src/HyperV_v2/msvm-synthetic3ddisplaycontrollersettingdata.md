---
description: Rappresenta le impostazioni per un controller di visualizzazione 3D sintetico per una macchina virtuale.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Classe Msvm_Synthetic3DDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310005"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a>\_Classe MSVM Synthetic3DDisplayControllerSettingData

Rappresenta le impostazioni per un controller di visualizzazione 3D sintetico per una macchina virtuale. Questa classe viene utilizzata solo con le macchine virtuali che utilizzano RemoteFX.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a>Members

La **classe \_ Synthetic3DDisplayControllerSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Synthetic3DDisplayControllerSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Si tratta di una proprietà di sola lettura, ma se la proprietà **ResourceType** è 20 (controller grafico), è possibile modificarla utilizzando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre. Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** . Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà allocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà deallocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dispositivo a cui è connessa la risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Si tratta di una proprietà di sola lettura, ma se 1) la proprietà **ResourceType** è 17 (porta seriale), o 2) la **Proprietà ResourceType** è 21 (extent di archiviazione) e la proprietà **ResourceSubType** è "Microsoft Virtual Hard Disk", può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Visibilità del consumer per la risorsa allocata. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)). Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice. Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità massima di risorse host corrispondenti che possono essere utilizzate dalla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MaximumMonitors**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero massimo di monitor disponibili per il controller di visualizzazione 3D. Il numero minimo di monitoraggi è 1 e il valore massimo dipende dalla risoluzione massima dello schermo. La tabella seguente definisce il numero massimo di monitoraggi consentiti per diverse risoluzioni.



| Soluzione            | Numero massimo di monitoraggi |
|-----------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

**MaximumScreenResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la risoluzione massima dello schermo per il controller di visualizzazione 3D. Deve essere uno dei valori seguenti.

<dt>

<span id="1024___768"></span>

<span id="1024___768"></span>**1024 \* 768** (0)


</dt> <dd>

La risoluzione massima è 1024 768.

</dd> <dt>

<span id="1280___1024"></span>

<span id="1280___1024"></span>**1280 \* 1024** (1)


</dt> <dd>

La risoluzione massima è 1280 1024.

</dd> <dt>

<span id="1600___1200"></span>

<span id="1600___1200"></span>**1600 \* 1200** (2)


</dt> <dd>

La risoluzione massima è 1600 1200.

</dd> <dt>

<span id="1920___1200"></span>

<span id="1920___1200"></span>**1920 \* 1200** (3)


</dt> <dd>

La risoluzione massima è 1920 1200.

</dd> <dt>

<span id="2560___1600"></span>

<span id="2560___1600"></span>**2560 \* 1600** (4)


</dt> <dd>

La risoluzione massima è 2650 1600.

</dd> <dt>

<span id="3840___2160"></span>

<span id="3840___2160"></span>**3840 \* 2160** (5)


</dt> <dd>

La risoluzione massima è 3840 2160.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016. MSVM \_ synte

 

</dd> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other). Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre della risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del pool di risorse da cui è stata allocata la risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità di risorse della CPU riservate per l'utilizzo da parte della macchina virtuale. Queste risorse sono sicuramente disponibili per l'utilizzo da parte della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risorsa rappresentata da questa impostazione di allocazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero totale di core nella macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'unità di misura per la proprietà **VirtualQuantity** . Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VRAMSizeBytes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Dimensioni della memoria del video per la macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

<dt>



 (67108864)


</dt> <dd></dd> <dt>



 (134217728)


</dt> <dd></dd> <dt>



 (268435456)


</dt> <dd></dd> <dt>



 (536870912)


</dt> <dd></dd> <dt>



 (1073741824)


</dt> <dd></dd> </dl>

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intero che definisce il peso per ogni processore di macchina virtuale. Una volta soddisfatte tutte le riservate, la capacità del processore fisico rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

0

Intervallo: 0 1000

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

