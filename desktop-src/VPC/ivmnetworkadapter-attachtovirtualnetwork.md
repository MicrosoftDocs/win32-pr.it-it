---
title: Metodo IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces.h)
description: Collega l'interfaccia di rete alla rete virtuale specificata.
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
ms.openlocfilehash: b03bf8bd0bcde6ba0353ce62e227c100a17ed1df0b2267ad54cd127c95c5836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593229"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>Metodo IVMNetworkAdapter::AttachToVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Collega l'interfaccia di rete alla rete virtuale specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualNetwork* \[ Pollici\]
</dt> <dd>

Rete virtuale a cui verrà connessa la scheda di interfaccia di rete virtuale. Vedere [**IVMVirtualNetwork.**](ivmvirtualnetwork.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | L'operazione è stata completata.<br/>                           |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **NULL.**<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | Il parametro non contiene una rete virtuale valida.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Accesso negato alla rete virtuale richiesta.<br/>     |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                          | La macchina virtuale non è valida o non esiste più.<br/>     |
| <dl> <dt>**VM \_ E ID DI RETE VIRTUALE NON \_ \_ \_ \_ VALIDO**</dt> </dl>                                                                        | Il parametro non è una rete virtuale esistente.<br/>       |
| <dl> <dt>**ECCEZIONE DISP \_ E \_**</dt> </dl>                                                                                          | Si è verificato un errore imprevisto.<br/>                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

