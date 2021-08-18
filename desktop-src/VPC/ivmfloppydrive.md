---
title: Interfaccia IVMFloppyDrive (VPCCOMInterfaces.h)
description: Controlla un'unità floppy all'interno di una macchina virtuale.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Interfaccia IVMFloppyDrive Virtual PC
- Interfaccia IVMFloppyDrive Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63db224861b547b9485b03080ce3ffb3f5c118ef0de71597db79aa0888a1528d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594807"
---
# <a name="ivmfloppydrive-interface"></a>Interfaccia IVMFloppyDrive

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controlla un'unità floppy all'interno di una macchina virtuale. **IVMFloppyDrive** può notificare ai client gli eventi usando l'interfaccia in uscita [**IVMFloppyDriveEvents.**](ivmfloppydriveevents.md) È possibile recuperare un **oggetto IVMFloppyDrive** dall'oggetto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) restituito dalla [**proprietà IVMVirtualMachine::FloppyDrives.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Membri

**L'interfaccia IVMFloppyDrive** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDrive** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMFloppyDrive** include questi metodi.



| Metodo                                                      | Descrizione                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Collega un'unità fisica nell'host all'unità floppy nella macchina virtuale.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Collega un'immagine del supporto floppy nell'host all'unità floppy.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Rilascia un'unità fisica nell'host dall'unità floppy.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Rilascia un'immagine del supporto floppy nell'host dall'unità floppy.<br/>                  |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IVMFloppyDrive.**



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Attachment**](ivmfloppydrive-attachment.md)<br/>           | Sola lettura<br/> | Tipo di supporto collegato all'unità floppy all'interno della macchina virtuale.<br/>     |
| [**Numero unità**](ivmfloppydrive-drivenumber.md)<br/>         | Sola lettura<br/> | Indice in base zero del controller a cui è collegata l'unità floppy.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Sola lettura<br/> | Lettera dell'unità host a cui è collegata l'unità floppy.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Sola lettura<br/> | Percorso completo del file di immagine a cui è collegata l'unità floppy.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive è definito come 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



 

