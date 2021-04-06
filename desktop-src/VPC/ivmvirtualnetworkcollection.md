---
title: Interfaccia IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Definisce una raccolta di oggetti IVMVirtualNetwork. Per ottenere un oggetto IVMVirtualNetworkCollection, usare la proprietà IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Interfaccia IVMVirtualNetworkCollection Virtual PC
- Interfaccia IVMVirtualNetworkCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743082"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interfaccia IVMVirtualNetworkCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce una raccolta di oggetti [**IVMVirtualNetwork**](ivmvirtualnetwork.md) . Per ottenere un oggetto **IVMVirtualNetworkCollection** , usare la proprietà [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualNetworkCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetworkCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMVirtualNetworkCollection** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                                                  |
| [**Conteggio**](ivmvirtualnetworkcollection-count.md)<br/>        | Sola lettura<br/> | Numero di reti virtuali in questa raccolta.<br/>                                                 |
| [**Elemento**](ivmvirtualnetworkcollection-item.md)<br/>          | Sola lettura<br/> | Oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4B2A-A21C-1982d8b0f675<br/> |



 

