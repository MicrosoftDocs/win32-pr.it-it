---
title: Metodo IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Connette l'interfaccia di rete alla rete virtuale specificata.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Metodo AttachToVirtualNetwork Virtual PC
- Metodo AttachToVirtualNetwork Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, metodo AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477188"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>Metodo IVMNetworkAdapter:: AttachToVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Connette l'interfaccia di rete alla rete virtuale specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualNetwork* \[ in\]
</dt> <dd>

Rete virtuale a cui verrà connessa la scheda di interfaccia di rete virtuale. Vedere [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                                                                       | L'operazione è stata completata.<br/>                           |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **null**.<br/>                              |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                               | Il parametro non contiene una rete virtuale valida.<br/> |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt> </dl> | Accesso negato alla rete virtuale richiesta.<br/>     |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                          | La macchina virtuale non è valida o non esiste più.<br/>     |
| <dl> <dt>**\_ \_ \_ \_ ID rete virtuale non valido E VM \_**</dt> </dl>                                                                        | Il parametro non è una rete virtuale esistente.<br/>       |
| <dl> <dt>**\_eccezione disp E \_**</dt> </dl>                                                                                          | Si è verificato un errore imprevisto.<br/>                       |



 

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

 

