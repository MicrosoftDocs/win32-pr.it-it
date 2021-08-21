---
title: Metodo IVMVirtualMachineEvents OnGuestLogoff (VPCCOMInterfaces.h)
description: Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Metodo OnGuestLogoff Virtual PC
- Metodo OnGuestLogoff Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnGuestLogoff
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81bdad6ffc75c33a0fa93146bd03f26442a71294cfdfc18536fdfacb6522363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056579"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a>Metodo IVMVirtualMachineEvents::OnGuestLogoff

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*logoffType* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione VMLogoffType**](vmlogofftype.md) che descrive il tipo di disconnessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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
</dt> <dt>

[**VMLogoffType**](vmlogofftype.md)
</dt> </dl>

 

