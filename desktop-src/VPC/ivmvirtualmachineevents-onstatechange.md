---
title: Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Riceve una notifica che lo stato di una macchina virtuale è stato modificato. | Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Metodo OnStateChange Virtual PC
- Metodo OnStateChange Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353821"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>Metodo IVMVirtualMachineEvents:: OnStateChange

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica che lo stato di una macchina virtuale è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualMachineState* \[ in\]
</dt> <dd>

Nuovo stato della macchina virtuale. Per un elenco di valori, vedere [**VMVMState**](vmvmstate.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene modificato lo stato della macchina virtuale. Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent StateChanged originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

