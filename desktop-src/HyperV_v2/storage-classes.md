---
description: 'Gli oggetti di archiviazione sono suddivisi in tre tipi: controller, unità e supporti.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Classi di archiviazione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c46efc17b3df5e1a509cec3565c6aaa7b65ff06d189951b100ac06d93a957e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829671"
---
# <a name="storage-classes"></a>Classi di archiviazione

Gli oggetti di archiviazione sono suddivisi in tre tipi: controller, unità e supporti.

Sono disponibili due controller, un controller IDE emulato e un controller SCSI sintetico. Entrambi i controller supportano l'allegato delle unità che ospitano il supporto.

Di seguito sono riportate le classi WMI di virtualizzazione correlate all'archiviazione. È disponibile anche il supporto per dischi floppy sintetici. Il collegamento a un'unità floppy fisica non è supportato.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dall'esecuzione.<br/>                                                                                               |
| [**Msvm \_ BasedOn**](msvm-basedon.md)<br/>                                           | Associazione che descrive come assemblare gli extent di archiviazione da extent di livello inferiore.<br/>                                                                                                           |
| [**Msvm \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.<br/>                                                                                                                          |
| [**Msvm \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Rappresenta un'unità disco rigido all'interno di una macchina virtuale.<br/>                                                                                                                                              |
| [**Msvm \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Rappresenta il controller floppy nella macchina virtuale.<br/>                                                                                                                                               |
| [**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Rappresenta un'unità floppy all'interno della macchina virtuale.<br/>                                                                                                                                                  |
| [**Unità \_ DVD Msvm**](msvm-dvddrive.md)<br/>                                         | Rappresenta un'unità DVD all'interno di una macchina virtuale.<br/>                                                                                                                                                    |
| [**Msvm \_ IDEController**](msvm-idecontroller.md)<br/>                               | Rappresenta un controller IDE.<br/>                                                                                                                                                                          |
| [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | Gestisce il supporto virtuale (file VHD, VHDX, ISO o VFD) per una macchina virtuale.<br/>                                                                                                                    |
| [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione.<br/>                                                                                                                             |
| [**Msvm \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Associa un'unità di archiviazione al supporto inserito nell'unità.<br/>                                                                                                                                     |
| [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Fornisce informazioni dettagliate su un'immagine di archiviazione montata manualmente.<br/>                                                                                                                                  |
| [**Protocollo \_ MsvmControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Questa associazione indica che una sottoclasse di dispositivo logico ,ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.<br/>                                                       |
| [**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Rappresenta un controller SCSI sintetico.<br/>                                                                                                                                                                |
| [**Msvm \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | Rappresenta un evento generato ogni volta che la **proprietà OperationalStatus** della [**classe Msvm \_ ResourcePool**](msvm-resourcepool.md) o [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) viene modificata.<br/> |
| [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Rappresenta le impostazioni correlate in modo specifico all'allocazione dell'archiviazione virtuale.<br/>                                                                                                                         |
| [**Processo di \_ archiviazione Msvm**](msvm-storagejob.md)<br/>                                     | Rappresenta un processo dell'operazione di archiviazione creato dal Microsoft Hyper-V di gestione delle immagini.<br/>                                                                                                          |
| [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Fornisce i dati di impostazione per un disco rigido virtuale.<br/>                                                                                                                                                         |
| [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.<br/>                                                                                                                                    |



 

 

 




