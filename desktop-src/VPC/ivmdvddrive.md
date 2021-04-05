---
title: Interfaccia IVMDVDDrive (VPCCOMInterfaces. h)
description: Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale. IVMDVDDrive può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Interfaccia IVMDVDDrive Virtual PC
- Interfaccia IVMDVDDrive Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048500"
---
# <a name="ivmdvddrive-interface"></a>Interfaccia IVMDVDDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale. **IVMDVDDrive** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .

È possibile aggiungere una nuova unità CD-ROM o DVD-ROM a una macchina virtuale usando il metodo [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) . È possibile rimuovere un'unità CD-ROM o DVD-ROM esistente da una macchina virtuale usando il metodo [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) . È possibile recuperare un oggetto **IVMDVDDrive** dall'oggetto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) restituito dalla proprietà [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMDVDDrive** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDrive** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMDVDDrive** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Connette un'unità host all'unità DVD all'interno della macchina virtuale.<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | Connette un'immagine ISO all'unità DVD all'interno della macchina virtuale.<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | Rilascia un'unità host acquisita dall'unità DVD.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Rilascia un'immagine ISO acquisita dall'unità DVD.<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMDVDDrive** ha queste proprietà.



| Proprietà                                                          | Tipo di accesso          | Descrizione                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Attachment**](ivmdvddrive-attachment.md)<br/>           | Sola lettura<br/> | Tipo di supporto collegato all'unità DVD all'interno della macchina virtuale.<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | Sola lettura<br/> | Numero del bus a cui è collegato il dispositivo.<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | Sola lettura<br/> | Numero del dispositivo a cui è collegata l'unità.<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | Sola lettura<br/> | Lettera dell'unità host impostata per questo dispositivo.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Sola lettura<br/> | Percorso completo del file di immagine impostato per il dispositivo.<br/>                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c<br/>                |



 

