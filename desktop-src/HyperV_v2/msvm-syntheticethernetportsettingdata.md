---
description: Rappresenta lo stato configurato di una scheda Ethernet sintetica.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Msvm_SyntheticEthernetPortSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d82c1826b865d94ae0a9a9d5a63fb535ad804ad5e874dec9563c5b5e74bd67f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949790"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a>Classe \_ Msvm SyntheticEthernetPortSettingData

Rappresenta lo stato configurato di una scheda Ethernet sintetica.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SyntheticEthernetPortSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SyntheticEthernetPortSettingData di Msvm** ha queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa. Ad esempio, l'indirizzo MAC di una porta Ethernet. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre. Le **proprietà Parent** **e AddressOnParent** vengono usate per descrivere la relazione tra controller e l'ordinamento dei dispositivi in un controller. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità di allocazione usate dalle **proprietà Reservation** **e Limit.** Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllowPacketDirect**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se la proiezione PacketDirect è abilitata per la macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà allocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà deallocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ClusterMonitored**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la scheda ethernet è monitorata da un cluster. Se non configurata, questa proprietà viene impostata su true per impostazione predefinita.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Oggetto a cui è connessa la risorsa. Ad esempio, una rete denominata o una porta del commutatore. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Visibilità dei consumer per la risorsa allocata. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 3 (virtualizzato).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità di configurazione desiderata per l'endpoint VLAN. Questa proprietà viene usata per impostare il valore iniziale della proprietà **OperationalEndpointMode** nell'istanza della classe [**\_ Msvm VLANEndpoint**](msvm-vlanendpoint.md) associata alla porta Ethernet di destinazione. Per i valori possibili, vedere la proprietà **OperationalEndpointMode** della **classe Msvm \_ VLANEndpoint.** Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData.**

</dd> <dt>

**DeviceNamingEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se questa scheda ethernet supporta la denominazione dei dispositivi.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il metodo [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**Risorsa host**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **Null.**

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

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Limite superiore o quantità massima di risorse che verrà concessa per questa allocazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il mapping di questa risorsa alle risorse sottostanti. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di modello di endpoint VLAN supportato da questo endpoint VLAN. Questa proprietà viene usata solo quando la **proprietà DesiredVLANEndpointMode** è impostata su 1 (Altro). Questa proprietà deve essere impostata **su Null** quando la **proprietà DesiredVLANEndpointMode** è un valore diverso da 1. Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData.**

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su "Altro" (0). Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e non viene usata.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre della risorsa. Ad esempio, un controller per l'allocazione corrente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**POOLID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Pool da cui la risorsa è attualmente allocata o da quale pool verrà allocata quando si verifica l'allocazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità di risorse garantita disponibile per questa allocazione. Nei sistemi che supportano l'over-commitment delle risorse, questo valore viene in genere usato per il controllo di ammissione per impedire l'accettazione di un'allocazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risorsa a cui si applica questa impostazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 10 (scheda Ethernet).

</dd> <dt>

**StaticMacAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se l'indirizzo MAC è statico.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità di risorse presentate al consumer. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'unità di misura per **la proprietà VirtualQuantity.** Il valore di questa proprietà deve essere un valore valido del qualificatore di unità programmatiche, come definito nell'allegato C.1 di DSP0004 V2.5 o versione successiva. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice di stringhe di identificatori di questa risorsa presentata al sistema operativo della macchina virtuale. Gli indici e i valori per indice vengono definiti per ogni risorsa, ovvero per ogni valore della proprietà **ResourceType** enumerata.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità relativa per questa allocazione in relazione ad altre allocazioni dallo stesso pool di risorse. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SyntheticEthernetPortSettingData di Msvm** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

Vedere [Esecuzione di query sugli oggetti di rete.](querying-networking-objects.md)

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

[**CIM \_ EthernetPortAllocationSettingData**](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

