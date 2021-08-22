---
title: Windows Interfacce di Virtual PC
description: Le interfacce seguenti sono supportate da Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC , interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963574a5293a7c48b29096e3dbc563c0f2073c7a697f84a86fa0b5750feeabe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511761"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Interfacce di Virtual PC

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Le interfacce seguenti sono supportate da Windows Virtual PC.



| Interfaccia                                                                             | Descrizione                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Fornisce l'accesso alle informazioni relative all'accounting per una macchina virtuale (VM).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Controlla le impostazioni di visualizzazione di una macchina virtuale.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMDVDDrive.**](ivmdvddrive.md)<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Controlla un'unità floppy all'interno di una macchina virtuale.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Definisce una raccolta di unità floppy all'interno della macchina virtuale.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMFloppyDrive.**](ivmfloppydrive.md)<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Definisce il sistema operativo guest in esecuzione all'interno di una macchina virtuale.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Fornisce l'accesso a un'immagine del disco rigido.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Definisce la connessione per un disco rigido all'interno della macchina virtuale.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Definisce la raccolta di connessioni al disco rigido all'interno della macchina virtuale.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Recupera informazioni sul computer host.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Controlla il dispositivo tastiera all'interno di una macchina virtuale.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Controlla il dispositivo mouse all'interno di una macchina virtuale.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Funge da interfaccia per una scheda di interfaccia di rete virtuale all'interno di una macchina virtuale.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Definisce una raccolta di schede di interfaccia di rete virtuali all'interno di una macchina virtuale.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Definisce una porta parallela all'interno di una macchina virtuale.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Definisce la raccolta di porte parallele all'interno della macchina virtuale.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Definisce una porta seriale all'interno di una macchina virtuale.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Definisce la raccolta di porte seriali all'interno della macchina virtuale.<br/>                                                  |
| [**Attività IVM**](ivmtask.md)<br/>                                                 | Consente di monitorare e controllare le attività asincrone per vari metodi.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Definisce la raccolta di oggetti attività all'interno di una macchina virtuale.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Definisce l'interfaccia per un dispositivo USB collegato al sistema host.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Definisce la raccolta di dispositivi USB collegati al sistema host.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Definisce l'interfaccia per una macchina virtuale.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Definisce la raccolta di macchine virtuali all'interno Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMVirtualMachine.**](ivmvirtualmachine.md)<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Definisce una rete virtuale.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Definisce una raccolta di [**oggetti IVMVirtualNetwork.**](ivmvirtualnetwork.md)<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Definisce la classe di primo livello Windows dell'applicazione Virtual PC.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMVirtualPC.**](ivmvirtualpc.md)<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Nota per gli sviluppatori in applicazioni a 64 bit Windows

Nelle edizioni a 64 bit di Windows la libreria dei tipi per Windows Virtual PC si trova in un file binario a 64 bit (VPC.exe) nella directory %WinDir% \\ System32. Questa directory non è visibile per impostazione predefinita ai processi a 32 bit. WOW64 esegue il mapping di tutti gli accessi alla directory %WinDir% \\ System32 alla directory %WinDir% \\ SysWOW64 per impostazione predefinita. Visual Studio è un file binario a 32 bit e pertanto non può aprire il file in questo percorso. Per generare un assembly di interoperabilità per Windows Virtual PC, usare TlbImp.exe, fornito con Visual Studio e Windows SDK. Per generare *Microsoft.VirtualPC.Interop.dll*, usare la riga di comando seguente:

**TlbImp.exe /out:** _Microsoft.VirtualPC.Interop.dll_ **/namespace:Microsoft.VirtualPC.Interop %WinDir% \\ System32 \\VPC.exe**

Altre soluzioni includono la copia di VPC.exe in una directory diversa in cui il compilatore può trovarlo o l'uso dello strumento OleView.exe da Windows SDK per estrarre un file con estensione idl dalla libreria dei tipi in VPC.exe.

 

