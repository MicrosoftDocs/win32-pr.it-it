---
title: Metodo IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces.h)
description: Riceve la notifica che l'heartbeat di una macchina virtuale è stato arrestato.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Metodo OnHeartbeatStopped Virtual PC
- Metodo OnHeartbeatStopped Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad4af982899f2f5f5dce6d78569323fbb6a85168c81b7c88c3ee0c62b3a39f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056589"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>Metodo IVMVirtualMachineEvents::OnHeartbeatStopped

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve la notifica che l'heartbeat di una macchina virtuale è stato arrestato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando il sistema operativo guest per questa macchina virtuale si è arrestato improvvisamente. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento heartbeat vmVirtualMachineEvent \_ originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

