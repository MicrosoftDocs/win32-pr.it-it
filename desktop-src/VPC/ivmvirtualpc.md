---
title: Interfaccia IVMVirtualPC (VPCCOMInterfaces. h)
description: Definisce l'oggetto applicazione Virtual PC Windows di livello superiore. Tutti gli altri oggetti dell'interfaccia di Windows Virtual PC vengono recuperati tramite questo oggetto.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Interfaccia IVMVirtualPC Virtual PC
- Interfaccia IVMVirtualPC Virtual PC, descritta
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
ms.openlocfilehash: 9d674fd1cbbe6c51881d15f91f0ebfb20f4f6749
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048489"
---
# <a name="ivmvirtualpc-interface"></a>Interfaccia IVMVirtualPC

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'oggetto applicazione Virtual PC Windows di livello superiore. Tutti gli altri oggetti dell'interfaccia di Windows Virtual PC vengono recuperati tramite questo oggetto.

**IVMVirtualPC** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMVirtualPCEvents**](ivmvirtualpcevents.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualPC** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPC** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMVirtualPC** dispone di questi metodi.



| Metodo                                                                                      | Descrizione                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Crea un disco rigido virtuale differenze.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Crea un disco rigido virtuale di ridimensionamento dinamico.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Crea un disco rigido virtuale a dimensione fissa.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Consente di creare un file di immagine disco floppy.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Elimina la configurazione di una macchina virtuale.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Recupera un oggetto rete virtuale che corrisponde al nome richiesto.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Recupera il valore dell'impostazione di configurazione specificata.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Recupera una matrice di file DVD noti.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Recupera una matrice di file di dischi floppy virtuali noti.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Recupera il tipo di un file di immagine del disco floppy esistente.<br/>                                     |
| [**Getharddisk**](ivmvirtualpc-getharddisk.md)                                             | Recupera un oggetto corrispondente a un file di immagine del disco esistente.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Recupera una matrice di file di disco rigido virtuale noti.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Recupera una matrice di file di configurazione della macchina virtuale noti.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Rimuove il valore dell'impostazione di configurazione specificata.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Imposta il valore dell'impostazione di configurazione specificata.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Annulla la registrazione di una configurazione di macchina virtuale senza eliminare il file di configurazione.<br/>          |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMVirtualPC** ha queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lettura/Scrittura<br/> | Directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Sola lettura<br/>  | Informazioni sul computer fisico.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Sola lettura<br/>  | Numero massimo di unità floppy per macchina virtuale.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Sola lettura<br/>  | Quantità massima di memoria fisica consentita per ogni macchina virtuale, in megabyte.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Sola lettura<br/>  | Numero massimo di interfacce di rete per macchina virtuale.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Sola lettura<br/>  | Numero massimo di bus consentiti per IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Sola lettura<br/>  | Numero massimo di porte parallele per macchina virtuale.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Sola lettura<br/>  | Numero massimo di porte seriali per macchina virtuale.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Sola lettura<br/>  | Quantità minima consentita di memoria fisica per macchina virtuale, in megabyte.<br/>                                                       |
| [**Nome**](ivmvirtualpc-name.md)<br/>                                               | Sola lettura<br/>  | Nome dell'applicazione Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lettura/Scrittura<br/> | Percorsi di file system utilizzati per individuare i file associati a Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Sola lettura<br/>  | Quantità massima di memoria fisica consentita suggerita per ogni macchina virtuale, in megabyte, per evitare condizioni di memoria insufficiente nell'host.<br/> |
| [**Attività**](ivmvirtualpc-tasks.md)<br/>                                             | Sola lettura<br/>  | Raccolta di attività.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Sola lettura<br/>  | Raccolta enumerabile di interfacce di rete non connesse.<br/>                                                                                |
| [**Tempo**](ivmvirtualpc-uptime.md)<br/>                                           | Sola lettura<br/>  | Numero di secondi in cui l'applicazione Windows Virtual PC è stata eseguita.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Sola lettura<br/>  | Raccolta enumerabile di tutti i dispositivi USB connessi all'host.<br/>                                                                         |
| [**Versione**](ivmvirtualpc-version.md)<br/>                                         | Sola lettura<br/>  | Versione di questa istanza di Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Sola lettura<br/>  | Raccolta enumerabile di macchine virtuali.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Sola lettura<br/>  | Raccolta enumerabile di reti virtuali.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



 

