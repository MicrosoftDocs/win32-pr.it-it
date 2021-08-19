---
title: Interfaccia IVMVirtualPC (VPCCOMInterfaces.h)
description: Definisce il livello principale dell'Windows dell'applicazione Virtual PC. Tutti gli Windows di interfaccia di Virtual PC vengono recuperati tramite questo oggetto .
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Interfaccia IVMVirtualPC Virtual PC
- Interfaccia IVMVirtualPC Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69dd5eec832e95b2b93ff0fb0bee026428a937fa277f86ff14ef672bc66e0dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124651"
---
# <a name="ivmvirtualpc-interface"></a>Interfaccia IVMVirtualPC

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce il livello principale dell'Windows dell'applicazione Virtual PC. Tutti gli Windows di interfaccia di Virtual PC vengono recuperati tramite questo oggetto .

**IVMVirtualPC** può inviare una notifica agli eventi ai client usando l'interfaccia in uscita [**IVMVirtualPCEvents.**](ivmvirtualpcevents.md)

## <a name="members"></a>Membri

**L'interfaccia IVMVirtualPC** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualPC** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IVMVirtualPC.**



| Metodo                                                                                      | Descrizione                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Crea un disco rigido virtuale differenze.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Crea un disco rigido virtuale ridimensionato dinamicamente.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Crea un disco rigido virtuale di dimensioni fisse.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Crea un file di immagine del disco floppy.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Elimina una configurazione di macchina virtuale.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Recupera un oggetto di rete virtuale che corrisponde al nome richiesto.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Recupera il valore dell'impostazione di configurazione specificata.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Recupera una matrice di file DVD noti.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Recupera una matrice di file di dischi floppy virtuali noti.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Recupera il tipo di un file di immagine del disco floppy esistente.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Recupera un oggetto corrispondente a un file di immagine disco esistente.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Recupera una matrice di file del disco rigido virtuale noti.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Recupera una matrice di file di configurazione di macchine virtuali noti.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Rimuove il valore dell'impostazione di configurazione specificata.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Imposta il valore dell'impostazione di configurazione specificata.<br/>                                        |
| [**Annullare la registrazione diVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Annulla la registrazione di una configurazione di macchina virtuale senza eliminare il file di configurazione.<br/>          |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IVMVirtualPC.**



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lettura/Scrittura<br/> | Directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.<br/>                                                    |
| [**Hostinfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Sola lettura<br/>  | Informazioni sul computer fisico.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Sola lettura<br/>  | Numero massimo di unità floppy per ogni macchina virtuale.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Sola lettura<br/>  | Quantità massima consentita di memoria fisica per ogni macchina virtuale, in megabyte.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Sola lettura<br/>  | Numero massimo di interfacce di rete per ogni macchina virtuale.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Sola lettura<br/>  | Numero massimo di bus consentiti per l'IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Sola lettura<br/>  | Numero massimo di porte parallele per ogni macchina virtuale.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Sola lettura<br/>  | Numero massimo di porte seriali per ogni macchina virtuale.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Sola lettura<br/>  | Quantità minima consentita di memoria fisica per ogni macchina virtuale, in megabyte.<br/>                                                       |
| [**Nome**](ivmvirtualpc-name.md)<br/>                                               | Sola lettura<br/>  | Nome dell'applicazione Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lettura/Scrittura<br/> | Percorsi file system usati per trovare i file associati a Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Sola lettura<br/>  | Quantità massima consentita massima consentita di memoria fisica per ogni macchina virtuale, in megabyte, per evitare condizioni di memoria insufficiente nell'host.<br/> |
| [**Attività**](ivmvirtualpc-tasks.md)<br/>                                             | Sola lettura<br/>  | Raccolta di attività.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Sola lettura<br/>  | Raccolta enumerabile di interfacce di rete non interconnesse.<br/>                                                                                |
| [**Uptime**](ivmvirtualpc-uptime.md)<br/>                                           | Sola lettura<br/>  | Numero di secondi durante i Windows'applicazione Virtual PC.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Sola lettura<br/>  | Raccolta enumerabile di tutti i dispositivi USB connessi all'host.<br/>                                                                         |
| [**Versione**](ivmvirtualpc-version.md)<br/>                                         | Sola lettura<br/>  | La versione di questa istanza di Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Sola lettura<br/>  | Raccolta enumerabile di macchine virtuali.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Sola lettura<br/>  | Raccolta enumerabile di reti virtuali.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



 

