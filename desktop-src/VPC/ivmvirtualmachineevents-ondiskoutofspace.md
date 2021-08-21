---
title: Metodo IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces.h)
description: Riceve una notifica che indica che lo spazio disponibile su un disco necessario per una macchina virtuale è insufficiente.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Metodo OnDiskOutOfSpace Virtual PC
- Metodo OnDiskOutOfSpace Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c482f0a713fda7e13436dc28d295469237273a7c607e522ce457ec908f210223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056629"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>Metodo IVMVirtualMachineEvents::OnDiskOutOfSpace

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che indica che lo spazio disponibile su un disco necessario per una macchina virtuale (VM) è insufficiente. Se lo spazio disponibile scende sotto i 100 MB, questo evento viene ricevuto come avviso e se lo spazio disponibile scende sotto i 20 MB questo evento viene ricevuto nuovamente come errore e la macchina virtuale verrà sospesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*criticallyLow* \[ Pollici\]
</dt> <dd>

Impostare **su VARIANT \_ TRUE** se il disco ha meno di 20 MB disponibili e su **VARIANT \_ FALSE** se lo spazio disponibile è superiore a 20 MB ma inferiore a 100 MB.

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

 

