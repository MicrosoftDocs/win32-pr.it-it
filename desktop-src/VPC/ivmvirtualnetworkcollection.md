---
title: Interfaccia IVMVirtualNetworkCollection (VPCCOMInterfaces.h)
description: Definisce una raccolta di oggetti IVMVirtualNetwork. Per ottenere un oggetto IVMVirtualNetworkCollection, usare la proprietà IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Interfaccia IVMVirtualNetworkCollection Virtual PC
- Interfaccia IVMVirtualNetworkCollection Virtual PC , descritto
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
ms.openlocfilehash: 32694b311482e58635ca28dc005fe68ab08495c15d251e176fb78266e7624e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592272"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interfaccia IVMVirtualNetworkCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce una raccolta di [**oggetti IVMVirtualNetwork.**](ivmvirtualnetwork.md) Per ottenere un **oggetto IVMVirtualNetworkCollection,** usare la [**proprietà IVMVirtualPC::VirtualNetworks.**](ivmvirtualpc-virtualnetworks.md)

## <a name="members"></a>Membri

**L'interfaccia IVMVirtualNetworkCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetworkCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili **nell'interfaccia IVMVirtualNetworkCollection.**



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                                                  |
| [**Conteggio**](ivmvirtualnetworkcollection-count.md)<br/>        | Sola lettura<br/> | Numero di reti virtuali in questa raccolta.<br/>                                                 |
| [**Elemento**](ivmvirtualnetworkcollection-item.md)<br/>          | Sola lettura<br/> | Oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



 

