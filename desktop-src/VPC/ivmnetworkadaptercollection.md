---
title: Interfaccia IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Definisce una raccolta di schede di interfaccia di rete virtuale. Per ottenere un oggetto IVMNetworkAdapterCollection, usare le proprietà IVMVirtualMachine I NetworkAdapter, IVMVirtualNetwork I NetworkAdapter e IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Interfaccia IVMNetworkAdapterCollection Virtual PC
- Interfaccia IVMNetworkAdapterCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048462"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Interfaccia IVMNetworkAdapterCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce una raccolta di schede di interfaccia di rete virtuale. Per ottenere un oggetto IVMNetworkAdapterCollection, usare le proprietà [**IVMVirtualMachine:: i NetworkAdapter**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: i NetworkAdapter**](ivmvirtualnetwork-networkadapters.md)e [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMNetworkAdapterCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapterCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMNetworkAdapterCollection** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                                                  |
| [**Conteggio**](ivmnetworkadaptercollection-count.md)<br/>        | Sola lettura<br/> | Numero di interfacce di rete in questa raccolta.<br/>                                               |
| [**Elemento**](ivmnetworkadaptercollection-item.md)<br/>          | Sola lettura<br/> | Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection è definito come ebaeafe9-EBCD-47CF-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine:: I NetworkAdapter**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork:: I NetworkAdapter**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

