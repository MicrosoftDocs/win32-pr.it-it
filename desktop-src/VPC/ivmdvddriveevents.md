---
title: Interfaccia IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Interfaccia IVMDVDDriveEvents Virtual PC
- Interfaccia IVMDVDDriveEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479012"
---
# <a name="ivmdvddriveevents-interface"></a>Interfaccia IVMDVDDriveEvents

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMDVDDrive**](ivmdvddrive.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMDVDDriveEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IVMDVDDriveEvents** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Riceve una notifica che segnala che il supporto è stato espulso dall'unità.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Riceve la notifica che i supporti sono stati inseriti nell'unità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



 

