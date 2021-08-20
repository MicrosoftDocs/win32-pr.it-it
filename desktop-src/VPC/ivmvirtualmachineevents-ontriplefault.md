---
title: Metodo IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces.h)
description: Riceve una notifica che indica che si è triplicato l'errore di una macchina virtuale.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Metodo OnTripleFault Virtual PC
- Metodo OnTripleFault Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9328ceff18256621a590bf0f235aca8ff12b142e4cdedf389d9d270bfde9bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122691"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a>Metodo IVMVirtualMachineEvents::OnTripleFault

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che indica che si è triplicato l'errore di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando si verifica un triplo errore in una macchina virtuale. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento TripleFault vmVirtualMachineEvent \_ originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

