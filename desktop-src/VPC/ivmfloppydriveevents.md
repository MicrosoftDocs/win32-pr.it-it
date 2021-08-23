---
title: Interfaccia IVMFloppyDriveEvents (VPCCOMInterfaces.h)
description: Definisce l'interfaccia eventi in uscita per l'interfaccia IVMFloppyDrive. Il client implementa questi metodi per ricevere gli eventi inviati da IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Interfaccia IVMFloppyDriveEvents Virtual PC
- Interfaccia IVMFloppyDriveEvents Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653511"
---
# <a name="ivmfloppydriveevents-interface"></a>Interfaccia IVMFloppyDriveEvents

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMFloppyDrive.**](ivmfloppydrive.md) Il client implementa questi metodi per ricevere eventi inviati da **IVMFloppyDrive.**

## <a name="members"></a>Membri

**L'interfaccia IVMFloppyDriveEvents** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveEvents** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IVMFloppyDriveEvents** include questi metodi.



| Metodo                                                      | Descrizione                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Riceve la notifica che il supporto è stato espulso dall'unità.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Riceve la notifica che il supporto è stato inserito nell'unità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

