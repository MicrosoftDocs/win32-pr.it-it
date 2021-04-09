---
title: Metodo IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Riceve una notifica di arresto dell'heartbeat di una macchina virtuale.
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
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964703"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>Metodo IVMVirtualMachineEvents:: OnHeartbeatStopped

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica di arresto dell'heartbeat di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando il sistema operativo guest per questa macchina virtuale si è arrestato in modo improvviso. Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent HeartbeatStopped originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

