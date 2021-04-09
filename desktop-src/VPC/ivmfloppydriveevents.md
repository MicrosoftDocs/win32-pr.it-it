---
title: Interfaccia IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMFloppyDrive. Il client implementa questi metodi per ricevere gli eventi inviati da IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Interfaccia IVMFloppyDriveEvents Virtual PC
- Interfaccia IVMFloppyDriveEvents Virtual PC, descritta
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
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121358"
---
# <a name="ivmfloppydriveevents-interface"></a>Interfaccia IVMFloppyDriveEvents

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMFloppyDrive**](ivmfloppydrive.md) . Il client implementa questi metodi per ricevere gli eventi inviati da **IVMFloppyDrive**.

## <a name="members"></a>Membri

L'interfaccia **IVMFloppyDriveEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IVMFloppyDriveEvents** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Riceve una notifica che segnala che il supporto è stato espulso dall'unità.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Riceve la notifica che i supporti sono stati inseriti nell'unità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

