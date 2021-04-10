---
title: Interfaccia IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controlla un'unità floppy all'interno di una macchina virtuale.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Interfaccia IVMFloppyDrive Virtual PC
- Interfaccia IVMFloppyDrive Virtual PC, descritta
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
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964773"
---
# <a name="ivmfloppydrive-interface"></a>Interfaccia IVMFloppyDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controlla un'unità floppy all'interno di una macchina virtuale. **IVMFloppyDrive** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) . È possibile recuperare un oggetto **IVMFloppyDrive** dall'oggetto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) restituito dalla proprietà [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMFloppyDrive** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDrive** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMFloppyDrive** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Connette un'unità fisica nell'host all'unità floppy della macchina virtuale.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Connette un'immagine multimediale floppy sull'host all'unità floppy.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Rilascia un'unità fisica nell'host dall'unità floppy.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Rilascia un'immagine di supporti floppy nell'host dall'unità floppy.<br/>                  |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMFloppyDrive** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Attachment**](ivmfloppydrive-attachment.md)<br/>           | Sola lettura<br/> | Tipo di supporto collegato all'unità floppy all'interno della macchina virtuale.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Sola lettura<br/> | Indice in base zero del controller a cui è collegata l'unità floppy.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Sola lettura<br/> | Lettera dell'unità host a cui è collegata l'unità floppy.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Sola lettura<br/> | Percorso completo del file di immagine a cui è collegata l'unità floppy.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e<br/>             |



 

