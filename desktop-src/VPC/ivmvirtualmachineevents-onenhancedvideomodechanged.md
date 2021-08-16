---
title: Metodo IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces.h)
description: Riceve una notifica che indica che il supporto di una macchina virtuale per la modalità video avanzata è stato modificato.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Metodo OnEnhancedVideoModeChanged Virtual PC
- Metodo OnEnhancedVideoModeChanged Virtual PC, interfaccia IVMVirtualMachineEvents
- Metodo OnEnhancedVideoModeChanged dell'interfaccia IVMVirtualMachineEvents
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bcdee9db2cf4b37b40d0cc77d6592c5ca1552b0a59642a01c2fe84bf4f69f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056619"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>Metodo IVMVirtualMachineEvents::OnEnhancedVideoModeChanged

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che indica che il supporto di una macchina virtuale per la modalità video avanzata è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*enhancedVideoMode* \[ Pollici\]
</dt> <dd>

Indica se è disponibile la modalità video avanzata.

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
</dt> </dl>

 

