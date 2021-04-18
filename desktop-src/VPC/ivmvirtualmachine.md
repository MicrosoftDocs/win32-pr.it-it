---
title: Interfaccia IVMVirtualMachine (VPCCOMInterfaces. h)
description: Definisce l'interfaccia per una macchina virtuale.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- Interfaccia IVMVirtualMachine Virtual PC
- Interfaccia IVMVirtualMachine Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006fe414a662c3d6d556aba68712aa0b428d9b5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300924"
---
# <a name="ivmvirtualmachine-interface"></a>Interfaccia IVMVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia per una macchina virtuale. **IVMVirtualMachine** può inviare notifiche ai client sugli eventi usando l'interfaccia in uscita [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) . Gli oggetti **IVMVirtualMachine** vengono restituiti dai metodi [**IVMVirtualPC**](ivmvirtualpc.md) , ad esempio [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md), [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)e [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md). È anche possibile recuperare un oggetto **IVMVirtualMachine** dall'oggetto [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md) restituito dalla proprietà [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualMachine** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachine** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMVirtualMachine** dispone di questi metodi.



| Metodo                                                                           | Descrizione                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Aggiunge una nuova unità CD o DVD alla macchina virtuale.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Aggiunge una nuova connessione al disco rigido alla macchina virtuale.<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Aggiunge un'interfaccia di rete alla macchina virtuale.<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | Connette un dispositivo USB a una macchina virtuale.<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | Rilascia un dispositivo USB da una macchina virtuale.<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | Elimina le informazioni sullo stato salvato per una macchina virtuale salvata.<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | Elimina i file modifiche disco virtuali.<br/>                                                                |
| [**GetActivationValue**](ivmvirtualmachine-getactivationvalue.md)               | Recupera il valore dell'impostazione di attivazione specificata per questa macchina virtuale.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Recupera il valore dell'impostazione di configurazione specificata per questa macchina virtuale.<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | Unisce i file modifiche disco virtuali.<br/>                                                                  |
| [**Sospendere**](ivmvirtualmachine-pause.md)                                         | Sospende la macchina virtuale.<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | Rimuove il valore dell'impostazione di attivazione specificata per questa macchina virtuale.<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Rimuove il valore dell'impostazione di configurazione specificata per questa macchina virtuale.<br/>              |
| [**RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Rimuove l'unità CD o DVD specificata dalla macchina virtuale.<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Rimuove la connessione al disco rigido specificata dalla macchina virtuale.<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | Rimuove un'interfaccia di rete dalla macchina virtuale.<br/>                                           |
| [**Reset**](ivmvirtualmachine-reset.md)                                         | Reimposta la macchina virtuale.<br/>                                                                     |
| [**Riprendi**](ivmvirtualmachine-resume.md)                                       | Riprende la macchina virtuale.<br/>                                                                    |
| [**Salva**](ivmvirtualmachine-save.md)                                           | Salva lo stato della macchina virtuale.<br/>                                                                |
| [**SetActivationValue**](ivmvirtualmachine-setactivationvalue.md)               | Imposta il valore dell'impostazione di attivazione specificata per questa macchina virtuale.<br/>                    |
| [**SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)         | Imposta il valore dell'impostazione di configurazione specificata per questa macchina virtuale.<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | Imposta un canale di comunicazione tra host e Guest.<br/>                                         |
| [**Avvio**](ivmvirtualmachine-startup.md)                                     | Avvia la macchina virtuale dallo stato non inizializzato o salvato.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Avvia la macchina virtuale dallo stato non inizializzato o salvato con opzioni avanzate.<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | Spegnimento della macchina virtuale.<br/>                                                                  |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMVirtualMachine** ha queste proprietà.



| Proprietà                                                                            | Tipo di accesso           | Descrizione                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Contabile**](ivmvirtualmachine-accountant.md)<br/>                       | Sola lettura<br/>  | Un contabile per questa macchina virtuale.<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Sola lettura<br/>  | Matrice che indica il tipo di unità collegata a ogni posizione della macchina virtuale.<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Lettura/Scrittura<br/> | Numero di serie della lavagna di base.<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | Lettura/Scrittura<br/> | GUID del BIOS.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Lettura/Scrittura<br/> | Numero di serie del BIOS.<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Lettura/Scrittura<br/> | Tag asset dello chassis.<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Lettura/Scrittura<br/> | Numero di serie dello chassis.<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | Sola lettura<br/>  | Identificatore univoco della macchina virtuale.<br/>                                                                                      |
| [**Visualizza**](ivmvirtualmachine-display.md)<br/>                             | Sola lettura<br/>  | Visualizzazione del video per la macchina virtuale.<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Sola lettura<br/>  | Raccolta enumerabile di unità CD e DVD collegate alla macchina virtuale.<br/>                                                      |
| [**File**](ivmvirtualmachine-file.md)<br/>                                   | Sola lettura<br/>  | Percorso completo del file. vmc per la configurazione della macchina virtuale.<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Sola lettura<br/>  | Raccolta enumerabile di unità floppy collegate alla macchina virtuale.<br/>                                                          |
| [**Guestos**](ivmvirtualmachine-guestos.md)<br/>                             | Sola lettura<br/>  | Sistema operativo guest per questa macchina virtuale.<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Sola lettura<br/>  | Raccolta enumerabile di connessioni disco rigido.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Sola lettura<br/>  | Indica se il processore supporta il set di istruzioni 3DNow.<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | Sola lettura<br/>  | Indica se il processore supporta il set di istruzioni MMX.<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | Sola lettura<br/>  | Indica se il processore supporta il set di istruzioni SSE.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Sola lettura<br/>  | Indica se il processore supporta il set di istruzioni SSE2.<br/>                                                                  |
| [**Tastiera**](ivmvirtualmachine-keyboard.md)<br/>                           | Sola lettura<br/>  | Il dispositivo della tastiera per la macchina virtuale.<br/>                                                                                        |
| [**Memoria**](ivmvirtualmachine-memory.md)<br/>                               | Lettura/Scrittura<br/> | Quantità di memoria fisica della macchina virtuale, in megabyte.<br/>                                                                 |
| [**Mouse**](ivmvirtualmachine-mouse.md)<br/>                                 | Sola lettura<br/>  | Il dispositivo mouse per la macchina virtuale.<br/>                                                                                           |
| [**Nome**](ivmvirtualmachine-name.md)<br/>                                   | Lettura/Scrittura<br/> | Nome della configurazione della macchina virtuale.<br/>                                                                                      |
| [**I NetworkAdapter**](ivmvirtualmachine-networkadapters.md)<br/>             | Sola lettura<br/>  | Raccolta enumerabile di schede di rete collegate alla macchina virtuale.<br/>                                                                   |
| [**Note**](ivmvirtualmachine-notes.md)<br/>                                 | Lettura/Scrittura<br/> | Note per la macchina virtuale.<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | Sola lettura<br/>  | Raccolta enumerabile di porte parallele.<br/>                                                                                         |
| [**ProcessorSpeed**](ivmvirtualmachine-processorspeed.md)<br/>               | Sola lettura<br/>  | Velocità del processore, in megahertz (MHz).<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | Sola lettura<br/>  | Nome della connessione RDP named pipe usato per video e input.<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Sola lettura<br/>  | Percorso completo del file di stato salvato.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Sola lettura<br/>  | Raccolta enumerabile di porte seriali.<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Lettura/Scrittura<br/> | Azione da eseguire su questa macchina virtuale se è in esecuzione quando viene chiuso il PC virtuale di Windows.<br/>                                |
| [**State**](ivmvirtualmachine-state.md)<br/>                                 | Sola lettura<br/>  | Stato corrente della macchina virtuale.<br/>                                                                                           |
| [**Annullabile**](ivmvirtualmachine-undoable.md)<br/>                           | Lettura/Scrittura<br/> | Indica se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale.<br/>                                      |
| [**UndoAction**](ivmvirtualmachine-undoaction.md)<br/>                       | Lettura/Scrittura<br/> | L'azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale viene arrestata dall'interno del sistema operativo guest.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



 

