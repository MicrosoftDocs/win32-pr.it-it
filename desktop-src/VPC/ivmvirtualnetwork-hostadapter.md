---
title: Proprietà IVMVirtualNetwork HostAdapter (VPCCOMInterfaces.h)
description: Nome della scheda a cui è connessa la rete virtuale.
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
ms.openlocfilehash: 72db5d8349572b2bd3549c2ee54d20e994bdfe8aed6ba0fbe31875e04f6942f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122681"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Proprietà IVMVirtualNetwork::HostAdapter

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il nome della scheda a cui è connessa la rete virtuale.

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
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                 | Il parametro è **NULL.**<br/>                                                                                                                                 |
| <dl> <dt>Macchina virtuale \_ E \_ ADAPTER NON TROVATO \_ \_ 0XA0040700</dt> <dt></dt> </dl> | La scheda Ethernet host a cui è stata connessa la rete virtuale non è più disponibile. La scheda Ethernet host potrebbe essere stata rimossa o disabilitata.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Si è verificato un errore imprevisto.<br/>                                                                                                                          |



## <a name="remarks"></a>Commenti

La scheda di rete virtuale consente a una rete virtuale di parlare con reti esterne. Nel computer host è in genere installata una scheda per ogni scheda Ethernet. Si supponga, ad esempio, che un computer host avesse un adattatore con etichetta "10/100 ENET". Per connettere una scheda di interfaccia di rete virtuale alla rete collegata a "10/100 ENET", impostare la proprietà **HostAdapter** di rete della rete virtuale su "10/100 ENET" e connettere la scheda di interfaccia di rete virtuale a questa rete virtuale.

Se la **proprietà HostAdapter** è impostata su una stringa vuota (""), la scheda di interfaccia di rete virtuale è connessa alla rete "Rete interna" o "Rete condivisa (NAT)". Le schede di interfaccia di rete virtuali collegate alla rete "Rete interna" non avranno accesso alle reti esterne nell'host di sistema. Tuttavia, le schede di interfaccia di rete virtuali collegate a questa rete virtuale sono ancora in grado di comunicare tra loro.

L'elenco completo delle schede è accessibile tramite la [**proprietà IVMHostInfo::NetworkAdapters.**](ivmhostinfo-networkadapters.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

