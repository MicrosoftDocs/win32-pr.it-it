---
title: Metodo IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
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
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302095"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>Metodo IVMVirtualMachine:: AddNetworkAdapter

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Aggiunge un'interfaccia di rete alla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapter* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                    | Il parametro *NetworkAdapter* è **null**.<br/>          |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>            | La configurazione è sconosciuta.<br/>                        |
| <dl> <dt>**Macchina virtuale \_ 0xA0040301 \_ \_ \_ valore non valido E pref**</dt> <dt></dt> </dl>   | Non è possibile aggiungere più di quattro schede di rete (4).<br/> |
| <dl> <dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>  |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>            | Si è verificato un errore imprevisto.<br/>                    |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere solo una nuova interfaccia di rete a una macchina virtuale arrestata. La scheda di rete appena creata non è connessa a una rete virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

