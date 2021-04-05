---
title: Metodo IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Riceve una notifica che indica che un disco richiesto per una macchina virtuale è insufficiente.
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
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873262"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>Metodo IVMVirtualMachineEvents:: OnDiskOutOfSpace

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica che indica che un disco necessario per una macchina virtuale (VM) ha esaurito lo spazio disponibile. Se lo spazio disponibile scende al di sotto di 100 MB, questo evento viene ricevuto come avviso e se lo spazio disponibile scende sotto 20 MB Questo evento viene ricevuto nuovamente come errore e la macchina virtuale verrà sospesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*criticallyLow* \[ in\]
</dt> <dd>

Impostare su **Variant \_ true** se il disco dispone di meno di 20 MB di spazio disponibile e di **Variant \_ false** se lo spazio disponibile è superiore a 20 MB ma inferiore a 100 MB.

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

 

