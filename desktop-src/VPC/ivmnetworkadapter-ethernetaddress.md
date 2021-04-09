---
title: Proprietà IVMNetworkAdapter EthernetAddress (VPCCOMInterfaces. h)
description: Indirizzo Ethernet (MAC) dell'interfaccia di rete.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Proprietà EthernetAddress Virtual PC
- Proprietà EthernetAddress Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, proprietà EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739759"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>Proprietà IVMNetworkAdapter:: EthernetAddress

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e imposta l'indirizzo Ethernet (MAC) dell'interfaccia di rete.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Valore proprietà

Indirizzo MAC della scheda di interfaccia di rete virtuale. Deve avere il *formato "XX XX XX* XX XX -  -  -  -  - ", dove ogni *X* è una cifra esadecimale.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_OK</dt> </dl>                                                                                                   | L'operazione è stata completata.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                              | Il parametro è **null**.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                           | Il formato del parametro non è corretto.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>Macchina virtuale \_ E \_ \_ set di \_ \_ \_ indirizzi MAC dinamici</dt> <dt>0xA004070A</dt> </dl> | L'indirizzo Ethernet per un'interfaccia di rete può essere generato in modo dinamico o può essere impostato su un indirizzo statico da parte dell'utente. Questo metodo non può essere chiamato quando l'indirizzo è impostato per essere generato in modo dinamico. La proprietà [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) viene usata per modificare il comportamento di generazione dell'indirizzo Ethernet.<br/> |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>                      | La macchina virtuale non è stata trovata. Questo problema può verificarsi se il computer è stato rimosso dopo la creazione dell'oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .<br/>                                                                                                                                                                                                                        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                      | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

