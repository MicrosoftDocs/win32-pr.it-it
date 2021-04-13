---
title: Metodo IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces. h)
description: Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Metodo OnEnhancedVideoModeChanged Virtual PC
- Metodo OnEnhancedVideoModeChanged Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnEnhancedVideoModeChanged
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
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475028"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>Metodo IVMVirtualMachineEvents:: OnEnhancedVideoModeChanged

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*enhancedVideoMode* \[ in\]
</dt> <dd>

Indica se è disponibile la modalità video avanzata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

 

