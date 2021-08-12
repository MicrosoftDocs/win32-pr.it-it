---
title: Interfaccia IVMVirtualNetwork (VPCCOMInterfaces.h)
description: Definisce una rete virtuale.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Interfaccia IVMVirtualNetwork Virtual PC
- Interfaccia IVMVirtualNetwork Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9caf5accb0add3354953d09e74a0893e2392deee7720b7a2cba0136b3f4b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592586"
---
# <a name="ivmvirtualnetwork-interface"></a>Interfaccia IVMVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce una rete virtuale. **Gli oggetti IVMVirtualNetwork** vengono restituiti dal [**metodo IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork.**](ivmvirtualpc-findvirtualnetwork.md) È anche possibile recuperare un **oggetto IVMVirtualNetwork** dall'oggetto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) restituito dalla [**proprietà IVMVirtualPC::VirtualNetworks.**](ivmvirtualpc-virtualnetworks.md)

Una rete virtuale è costituita da un commutatore virtuale, che esegue tutto il routing interno, e da diverse connessioni "collegate" al commutatore virtuale. Queste connessioni possono essere una connessione host esterna reale, una "rete interna" o una rete condivisa (NAT).

## <a name="members"></a>Membri

**L'interfaccia IVMVirtualNetwork** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetwork** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMVirtualNetwork** include questi metodi.



| Metodo                                | Descrizione                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_ID**](ivmvirtualnetwork--id.md) | Recupera l'identificatore interno della rete virtuale.<br/> |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IVMVirtualNetwork.**



| Proprietà                                                                | Tipo di accesso          | Descrizione                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Sola lettura<br/> | Nome della scheda a cui è connessa la rete virtuale.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Sola lettura<br/> | Determina se l'istanza di rete virtuale è wireless o meno.<br/> |
| [**Nome**](ivmvirtualnetwork-name.md)<br/>                       | Sola lettura<br/> | Nome univoco dell'istanza di rete virtuale.<br/>                    |
| [**Oggetti NetworkAdapter**](ivmvirtualnetwork-networkadapters.md)<br/> | Sola lettura<br/> | Raccolta enumerabile di schede di interfaccia di rete collegate alla rete virtuale.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

