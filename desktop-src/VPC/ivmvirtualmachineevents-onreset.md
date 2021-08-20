---
title: Metodo OnReset IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Riceve la notifica che una macchina virtuale è stata reimpostata.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Metodo OnReset Virtual PC
- Metodo OnReset Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnReset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4101885469de59a7cd2740dc07db44101ce130df037540306f4afdab78c80fd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122904"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a>Metodo IVMVirtualMachineEvents::OnReset

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve la notifica che una macchina virtuale è stata reimpostata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnReset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando la macchina virtuale è stata reimpostata. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento vmVirtualMachineEvent \_ Reset originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

