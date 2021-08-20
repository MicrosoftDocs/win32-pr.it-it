---
title: Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces.h)
description: Riceve una notifica che indica che lo stato di una macchina virtuale è stato modificato. | Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 1cf966d2439f3095051331b5412bc92cca9ba76e6f98c9777402ba449f2e7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122701"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>Metodo IVMVirtualMachineEvents::OnStateChange

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che indica che lo stato di una macchina virtuale è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualMachineState* \[ Pollici\]
</dt> <dd>

Nuovo stato della macchina virtuale. Per un elenco di valori, vedere [**VMVMState.**](vmvmstate.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando lo stato di questa macchina virtuale cambia. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento vmVirtualMachineEvent \_ StateChanged proveniente da [**IVMVirtualMachine.**](ivmvirtualmachine.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

