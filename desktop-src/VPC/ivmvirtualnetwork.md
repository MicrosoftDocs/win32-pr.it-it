---
title: Interfaccia IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Definisce una rete virtuale.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Interfaccia IVMVirtualNetwork Virtual PC
- Interfaccia IVMVirtualNetwork Virtual PC, descritta
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
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302550"
---
# <a name="ivmvirtualnetwork-interface"></a>Interfaccia IVMVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce una rete virtuale. Gli oggetti **IVMVirtualNetwork** vengono restituiti dal metodo [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md). È anche possibile recuperare un oggetto **IVMVirtualNetwork** dall'oggetto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) restituito dalla proprietà [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

Una rete virtuale è costituita da un commutire virtuale, che esegue tutti i routing interni e diverse connessioni "collegate" al commutere virtuale. Queste connessioni possono essere una connessione host esterna reale, una rete interna o una rete condivisa (NAT).

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualNetwork** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetwork** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMVirtualNetwork** dispone di questi metodi.



| Metodo                                | Descrizione                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_ID**](ivmvirtualnetwork--id.md) | Recupera l'identificatore interno della rete virtuale.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMVirtualNetwork** ha queste proprietà.



| Proprietà                                                                | Tipo di accesso          | Descrizione                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Sola lettura<br/> | Nome dell'adapter a cui è connessa la rete virtuale.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Sola lettura<br/> | Determina se l'istanza della rete virtuale è wireless o meno.<br/> |
| [**Nome**](ivmvirtualnetwork-name.md)<br/>                       | Sola lettura<br/> | Nome univoco dell'istanza di rete virtuale.<br/>                    |
| [**I NetworkAdapter**](ivmvirtualnetwork-networkadapters.md)<br/> | Sola lettura<br/> | Raccolta enumerabile di schede di rete collegate alla rete virtuale.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

