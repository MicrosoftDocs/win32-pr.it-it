---
title: Proprietà IVMVirtualMachine AttachedDriveTypes (VPCCOMInterfaces. h)
description: Matrice che indica il tipo di unità collegata a ogni posizione della macchina virtuale.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Proprietà AttachedDriveTypes Virtual PC
- Proprietà AttachedDriveTypes Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà AttachedDriveTypes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121087"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a>Proprietà IVMVirtualMachine:: AttachedDriveTypes

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matrice che indica il tipo di unità collegata a ogni posizione della macchina virtuale (VM).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a>Valore proprietà

Variante di tipo VT **\_ Array** VT \| **\_ Variant** contenente voci di tipo **VT \_ Ui1**. La matrice contiene il valore [**VMDriveType**](vmdrivetype.md) di ogni dispositivo connesso a ogni percorso del bus. La matrice viene ordinata in base a \[ *busNumber* \] \[ *DeviceID* \] .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl> | La configurazione è sconosciuta.<br/>     |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

