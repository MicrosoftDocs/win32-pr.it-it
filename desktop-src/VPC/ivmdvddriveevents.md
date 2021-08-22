---
title: Interfaccia IVMDVDDriveEvents (VPCCOMInterfaces.h)
description: Definisce l'interfaccia eventi in uscita per l'interfaccia IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Interfaccia IVMDVDDriveEvents Virtual PC
- Interfaccia IVMDVDDriveEvents Virtual PC , descritta
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
ms.openlocfilehash: dcb34bf77b6692c90977262ac7e2177019169e3195ee44415a0693102e6d15ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136794"
---
# <a name="ivmdvddriveevents-interface"></a>Interfaccia IVMDVDDriveEvents

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMDVDDrive.**](ivmdvddrive.md)

## <a name="members"></a>Membri

**L'interfaccia IVMDVDDriveEvents** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveEvents** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IVMDVDDriveEvents** include questi metodi.



| Metodo                                                   | Descrizione                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Riceve la notifica che il supporto è stato espulso dall'unità.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Riceve una notifica che indica che i supporti sono stati inseriti nell'unità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



 

