---
title: Proprietà IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nome dell'adapter a cui è connessa la rete virtuale.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Proprietà HostAdapter Virtual PC
- Proprietà HostAdapter Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, proprietà HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048621"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Proprietà IVMVirtualNetwork:: HostAdapter

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il nome dell'adapter a cui è connessa la rete virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Valore proprietà

Nome della scheda host a cui è connessa la rete virtuale.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                            | Significato                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | L'operazione è stata completata.<br/>                                                                                                                              |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                 | Il parametro è **null**.<br/>                                                                                                                                 |
| <dl> <dt>Macchina virtuale \_ L' \_ adapter \_ E \_ non</dt> è stato trovato <dt>0xA0040700</dt> </dl> | La scheda Ethernet host a cui è connessa la rete virtuale non è più disponibile. La scheda Ethernet host potrebbe essere stata rimossa o disabilitata.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>         | Si è verificato un errore imprevisto.<br/>                                                                                                                          |



## <a name="remarks"></a>Commenti

La scheda di rete virtuale consente a una rete virtuale di comunicare con reti esterne. In genere, una scheda per ogni scheda Ethernet è installata nel computer host. Supponiamo, ad esempio, che un computer host disponga di un adattatore con etichetta "10/100 ENET". Per connettere una scheda di interfaccia di rete virtuale alla rete collegata a "10/100 ENET", impostare la proprietà Network **hostadapter** della rete virtuale su "10/100 ENET" e connettere la scheda di interfaccia di rete virtuale a questa rete virtuale.

Se la proprietà **hostadapter** è impostata su una stringa vuota (""), la scheda NIC virtuale è connessa alla rete "rete interna" o "rete di rete condivisa (NAT)". Le schede di rete virtuali collegate alla rete "rete interna" non avranno accesso alle reti esterne nell'host di sistema. Tuttavia, le schede di rete virtuali collegate a questa rete virtuale sono ancora in grado di comunicare tra loro.

È possibile accedere all'elenco completo degli adapter tramite la proprietà [**IVMHostInfo:: i NetworkAdapter**](ivmhostinfo-networkadapters.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

