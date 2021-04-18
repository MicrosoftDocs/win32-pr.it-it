---
description: 'Gli oggetti di archiviazione sono suddivisi in tre tipi: controller, unità e supporti.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Classi di archiviazione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c17ad2530a86e7f404fe19eaeb3ef5a1cd7895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317186"
---
# <a name="storage-classes"></a>Classi di archiviazione

Gli oggetti di archiviazione sono suddivisi in tre tipi: controller, unità e supporti.

Sono disponibili due controller, un controller IDE emulato e un controller SCSI sintetico. Entrambi i controller supportano l'allegato di unità che ospitano i supporti.

Di seguito sono riportate le classi WMI di virtualizzazione correlate all'archiviazione. È disponibile anche il supporto per supporti disco floppy sintetici. La connessione a un'unità floppy fisica non è supportata.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AffectedStorageJobElement MSVM**](msvm-affectedstoragejobelement.md)<br/>       | Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dalla relativa esecuzione.<br/>                                                                                               |
| [**\_BasedOn MSVM**](msvm-basedon.md)<br/>                                           | Associazione che descrive come possono essere assemblati gli extent di archiviazione dagli extent di livello inferiore.<br/>                                                                                                           |
| [**\_ControlledBy MSVM**](msvm-controlledby.md)<br/>                                 | Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.<br/>                                                                                                                          |
| [**\_DiskDrive MSVM**](msvm-diskdrive.md)<br/>                                       | Rappresenta un'unità disco rigido all'interno di una macchina virtuale.<br/>                                                                                                                                              |
| [**\_DisketteController MSVM**](msvm-diskettecontroller.md)<br/>                     | Rappresenta il controller floppy nella macchina virtuale.<br/>                                                                                                                                               |
| [**\_DisketteDrive MSVM**](msvm-diskettedrive.md)<br/>                               | Rappresenta un'unità floppy all'interno della macchina virtuale.<br/>                                                                                                                                                  |
| [**\_DVDDrive MSVM**](msvm-dvddrive.md)<br/>                                         | Rappresenta un'unità DVD all'interno di una macchina virtuale.<br/>                                                                                                                                                    |
| [**\_IDECONTROLLER MSVM**](msvm-idecontroller.md)<br/>                               | Rappresenta un controller IDE.<br/>                                                                                                                                                                          |
| [**\_Servizio MSVM**](msvm-imagemanagementservice.md)<br/>             | Gestisce i file multimediali virtuali (file con estensione VHD, VHDX, ISO o VFD) per una macchina virtuale.<br/>                                                                                                                    |
| [**\_Disco logico MSVM**](msvm-logicaldisk.md)<br/>                                   | Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione.<br/>                                                                                                                             |
| [**\_MediaPresent MSVM**](msvm-mediapresent.md)<br/>                                 | Associa un'unità di archiviazione al supporto inserito nell'unità.<br/>                                                                                                                                     |
| [**\_MountedStorageImage MSVM**](msvm-mountedstorageimage.md)<br/>                   | Fornisce informazioni dettagliate su un'immagine di archiviazione montata manualmente.<br/>                                                                                                                                  |
| [**\_ProtocolControllerForUnit MSVM**](msvm-protocolcontrollerforunit.md)<br/>       | Questa associazione indica che una sottoclasse di un dispositivo logico, ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.<br/>                                                       |
| [**\_SCSIProtocolController MSVM**](msvm-scsiprotocolcontroller.md)<br/>             | Rappresenta un controller SCSI sintetico.<br/>                                                                                                                                                                |
| [**\_StorageAlert MSVM**](msvm-storagealert.md)<br/>                                 | Rappresenta un evento generato ogni volta che viene modificata la proprietà **OperationalStatus** della classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ disco logico**](msvm-logicaldisk.md) .<br/> |
| [**\_StorageAllocationSettingData MSVM**](msvm-storageallocationsettingdata.md)<br/> | Rappresenta le impostazioni specifiche relative all'allocazione di archiviazione virtuale.<br/>                                                                                                                         |
| [**\_StorageJob MSVM**](msvm-storagejob.md)<br/>                                     | Rappresenta un processo dell'operazione di archiviazione creato dal servizio gestione immagini Microsoft Hyper-V.<br/>                                                                                                          |
| [**\_VirtualHardDiskSettingData MSVM**](msvm-virtualharddisksettingdata.md)<br/>     | Fornisce i dati di impostazione per un disco rigido virtuale.<br/>                                                                                                                                                         |
| [**\_VirtualHardDiskState MSVM**](msvm-virtualharddiskstate.md)<br/>                 | Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.<br/>                                                                                                                                    |



 

 

 




