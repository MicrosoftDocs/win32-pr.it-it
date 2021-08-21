---
title: Metodo IVMVirtualMachineEvents OnAdditionsUninstalled (VPCCOMInterfaces.h)
description: Riceve la notifica che i componenti di integrazione vengono disinstallati in una macchina virtuale.
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- Metodo OnAdditionsUninstalled Virtual PC
- Metodo OnAdditionsUninstalled Virtual PC , interfaccia IVMVirtualMachineEvents
- Metodo OnAdditionsUninstalled dell'interfaccia IVMVirtualMachineEvents
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0371ea41c22f24ee2dd21e1a41166f839af8fce2aa84d58a7844d4e11f0bbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056729"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a>Metodo IVMVirtualMachineEvents::OnAdditionsUninstalled

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve la notifica che i componenti di integrazione vengono disinstallati in una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

