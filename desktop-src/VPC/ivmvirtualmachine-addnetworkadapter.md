---
title: Metodo IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces.h)
description: Aggiunge un'interfaccia di rete alla macchina virtuale.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Metodo AddNetworkAdapter Virtual PC
- Metodo AddNetworkAdapter Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799aa859ab8cd2bea4da29154af00c6537bfd180b0719f6d0252b1b0ddea8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866740"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>Metodo IVMVirtualMachine::AddNetworkAdapter

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Aggiunge un'interfaccia di rete alla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*networkAdapter* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMNetworkAdapter.**](ivmnetworkadapter.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                    | Il *parametro networkAdapter* è **NULL.**<br/>          |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                        |
| <dl> <dt>**Macchina virtuale \_ VALORE \_ PREF \_ NON VALIDO \_ 0xA0040301**</dt> <dt></dt> </dl>   | Non è possibile aggiungere più di quattro (4) schede di rete.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ VM RUNNING OR \_ \_ \_ SAVED**</dt> <dt>0xA004020B</dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>  |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                    |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere una nuova interfaccia di rete solo a una macchina virtuale arrestata. La scheda di rete appena creata non è connessa a una rete virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

