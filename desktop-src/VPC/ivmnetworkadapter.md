---
title: Interfaccia IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Funge da interfaccia per una scheda di interfaccia di rete virtuale.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Interfaccia IVMNetworkAdapter Virtual PC
- Interfaccia IVMNetworkAdapter Virtual PC, descritta
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
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400669"
---
# <a name="ivmnetworkadapter-interface"></a>Interfaccia IVMNetworkAdapter

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Funge da interfaccia per una scheda di interfaccia di rete virtuale (NIC). Viene usato per configurare la modalità di rete di una macchina virtuale. È possibile aggiungere e rimuovere schede di interfaccia di rete usando [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). È anche possibile recuperare un oggetto **IVMNetworkAdapter** dalla raccolta [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) restituito dalle proprietà [**IVMVirtualMachine:: I NetworkAdapter**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork:: i NetworkAdapter**](ivmvirtualnetwork-networkadapters.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMNetworkAdapter** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMNetworkAdapter** dispone di questi metodi.



| Metodo                                                                         | Descrizione                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_ID**](ivmnetworkadapter--id.md)                                          | Recupera l'identificatore interno di questa interfaccia di rete.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Connette l'interfaccia di rete alla rete virtuale specificata.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Scollega l'interfaccia di rete dalla relativa rete virtuale.<br/>         |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMNetworkAdapter** ha queste proprietà.



| Proprietà                                                                                  | Tipo di accesso           | Descrizione                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lettura/Scrittura<br/> | Indirizzo Ethernet (MAC) dell'interfaccia di rete.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lettura/Scrittura<br/> | Indica se l'indirizzo Ethernet viene generato dinamicamente.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Sola lettura<br/>  | Macchina virtuale associata a questa interfaccia di rete.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Sola lettura<br/>  | Rete virtuale a cui è collegata l'interfaccia di rete.<br/>  |



 

## <a name="remarks"></a>Commenti

L'indirizzo Ethernet predefinito per un'interfaccia di rete è "00-00-00-00-00-00", che è considerato un indirizzo Ethernet non valido per la maggior parte dei sistemi operativi. Se [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) è impostato su **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) deve essere inizializzato con un indirizzo di rete Ethernet valido.

Nelle procedure riportate di seguito viene illustrato come utilizzare l'interfaccia **IVMNetworkAdapter** .

**Per alleghi una scheda di interfaccia di rete virtuale a una NIC host**

-   Le NIC virtuali (Guest) non sono collegate direttamente a una scheda di interfaccia di rete host. La scheda di interfaccia di rete virtuale è invece collegata a una rete virtuale collegata a una scheda di interfaccia di rete host. Per ulteriori informazioni sulla configurazione delle reti virtuali, vedere [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Per alleghi la scheda di interfaccia di rete virtuale a una rete virtuale, usare il metodo [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .

**Per disconnettere una scheda di interfaccia di rete virtuale dalla rete virtuale**

-   Il metodo [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) scollega la scheda di interfaccia di rete virtuale dalla rete virtuale. Dopo la chiamata a questa funzione, la proprietà [**virtualnetwork**](ivmnetworkadapter-virtualnetwork.md) restituirà un ID di rete virtuale non valido.

**Per rimuovere una scheda di interfaccia di rete virtuale da una macchina virtuale se si dispone dell'oggetto NIC virtuale**

1.  Ottenere la macchina virtuale associata alla scheda di interfaccia di rete virtuale usando la proprietà [**virtualmachine**](ivmnetworkadapter-virtualmachine.md) .
2.  Usare l'oggetto corrente come parametro per il metodo [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



 

