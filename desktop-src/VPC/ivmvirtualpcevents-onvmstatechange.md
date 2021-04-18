---
title: Metodo IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Riceve una notifica che lo stato di una macchina virtuale è stato modificato. | Metodo IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Metodo OnVMStateChange Virtual PC
- Metodo OnVMStateChange Virtual PC, interfaccia IVMVirtualPCEvents
- Interfaccia IVMVirtualPCEvents Virtual PC, metodo OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321540"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>Metodo IVMVirtualPCEvents:: OnVMStateChange

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica che lo stato di una macchina virtuale è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualMachineConfig* \[ in\]
</dt> <dd>

Nome della macchina virtuale.

</dd> <dt>

*virtualMachineState* \[ in\]
</dt> <dd>

Nuovo stato della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualPCEvent \_ VMStateChanged** originato da [**IVMVirtualPC**](ivmvirtualpc.md). Per monitorare una macchina virtuale specifica, usare il metodo [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

