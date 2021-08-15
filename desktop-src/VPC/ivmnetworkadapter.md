---
title: Interfaccia IVMNetworkAdapter (VPCCOMInterfaces.h)
description: Funge da interfaccia per una scheda di interfaccia di rete virtuale.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Interfaccia IVMNetworkAdapter Virtual PC
- Interfaccia IVMNetworkAdapter Virtual PC , descritta
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73622161629f6d3746c153fb9e2df32ee120fd748defc60d0d02ef6ea4378b14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118843898"
---
# <a name="ivmnetworkadapter-interface"></a>Interfaccia IVMNetworkAdapter

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Funge da interfaccia per una scheda di interfaccia di rete virtuale. Viene usato per configurare la modalità di rete di una macchina virtuale. È possibile aggiungere e rimuovere schede di interfaccia di rete usando [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). È anche possibile recuperare un oggetto **IVMNetworkAdapter** dalla raccolta [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) restituita dalle proprietà [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork::NetworkAdapters.**](ivmvirtualnetwork-networkadapters.md)

## <a name="members"></a>Membri

**L'interfaccia IVMNetworkAdapter** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMNetworkAdapter** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMNetworkAdapter** dispone di questi metodi.



| Metodo                                                                         | Descrizione                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_ID**](ivmnetworkadapter--id.md)                                          | Recupera l'identificatore interno di questa interfaccia di rete.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Collega l'interfaccia di rete alla rete virtuale specificata.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Scollega l'interfaccia di rete dalla rete virtuale.<br/>         |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IVMNetworkAdapter.**



| Proprietà                                                                                  | Tipo di accesso           | Descrizione                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lettura/Scrittura<br/> | Indirizzo Ethernet (MAC) dell'interfaccia di rete.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lettura/Scrittura<br/> | Indica se l'indirizzo Ethernet viene generato dinamicamente.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Sola lettura<br/>  | Macchina virtuale associata a questa interfaccia di rete.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Sola lettura<br/>  | Rete virtuale a cui è collegata l'interfaccia di rete.<br/>  |



 

## <a name="remarks"></a>Commenti

L'indirizzo Ethernet predefinito per un'interfaccia di rete è "00-00-00-00-00-00", che viene considerato un indirizzo Ethernet non valido dalla maggior parte dei sistemi operativi. Se [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) è impostato su **FALSE,** [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) deve essere inizializzato con un indirizzo di rete Ethernet valido.

Le procedure seguenti illustrano come usare **l'interfaccia IVMNetworkAdapter.**

**Per collegare una scheda di interfaccia di rete virtuale a una scheda di interfaccia di rete host**

-   Le schede di interfaccia di rete virtuali (guest) non sono collegate direttamente a una scheda di interfaccia di rete host. Al contrario, la scheda di interfaccia di rete virtuale è collegata a una rete virtuale collegata a una scheda di interfaccia di rete host. Per altre informazioni sulla configurazione delle reti virtuali, vedere [**IVMVirtualNetwork.**](ivmvirtualnetwork.md) Per collegare la scheda di interfaccia di rete virtuale a una rete virtuale, usare [**il metodo AttachToVirtualNetwork.**](ivmnetworkadapter-attachtovirtualnetwork.md)

**Per disconnettere una scheda di interfaccia di rete virtuale dalla rete virtuale**

-   Il [**metodo DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) scollega la scheda di interfaccia di rete virtuale dalla rete virtuale. Dopo la chiamata a questa funzione, la [**proprietà VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) restituirà un ID di rete virtuale non valido.

**Per rimuovere una scheda di interfaccia di rete virtuale da una macchina virtuale se si dispone dell'oggetto nic virtuale**

1.  Ottenere la macchina virtuale associata alla scheda di interfaccia di rete virtuale usando la [**proprietà VirtualMachine.**](ivmnetworkadapter-virtualmachine.md)
2.  Usare l'oggetto corrente come parametro per [**il metodo IVMVirtualMachine::RemoveNetworkAdapter.**](ivmvirtualmachine-removenetworkadapter.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



 

