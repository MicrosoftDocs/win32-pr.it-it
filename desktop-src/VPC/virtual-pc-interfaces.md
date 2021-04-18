---
title: Interfacce Virtual PC Windows
description: Le interfacce seguenti sono supportate da Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299896"
---
# <a name="windows-virtual-pc-interfaces"></a>Interfacce Virtual PC Windows

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Le interfacce seguenti sono supportate da Windows Virtual PC.



| Interfaccia                                                                             | Descrizione                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Consente di accedere alle informazioni relative all'accounting per una macchina virtuale (VM).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Controlla le impostazioni di visualizzazione di una macchina virtuale.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Controlla un'unità CD-ROM o DVD-ROM all'interno di una macchina virtuale.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMDVDDrive**](ivmdvddrive.md) .<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Controlla un'unità floppy all'interno di una macchina virtuale.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Definisce una raccolta di unità floppy all'interno della macchina virtuale.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMFloppyDrive**](ivmfloppydrive.md) .<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Definisce il sistema operativo guest in esecuzione all'interno di una macchina virtuale.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Consente di accedere a un'immagine del disco rigido.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Definisce la connessione per un disco rigido all'interno della macchina virtuale.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Definisce la raccolta di connessioni del disco rigido all'interno della macchina virtuale.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Recupera le informazioni sul computer host.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Controlla il dispositivo della tastiera all'interno di una macchina virtuale.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Controlla il dispositivo mouse all'interno di una macchina virtuale.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Funge da interfaccia per una scheda di interfaccia di rete virtuale (NIC) in una macchina virtuale.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Definisce una raccolta di schede di rete virtuali all'interno di una macchina virtuale.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Definisce una porta parallela all'interno di una macchina virtuale.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Definisce la raccolta di porte parallele all'interno della macchina virtuale.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Definisce una porta seriale all'interno di una macchina virtuale.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Definisce la raccolta di porte seriali all'interno della macchina virtuale.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Utilizzato per monitorare e controllare le attività asincrone per diversi metodi.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Definisce la raccolta di oggetti attività all'interno di una macchina virtuale.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Definisce l'interfaccia per un dispositivo USB collegato al sistema host.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Definisce la raccolta di dispositivi USB collegati al sistema host.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Definisce l'interfaccia per una macchina virtuale.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Definisce la raccolta di macchine virtuali all'interno di Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualMachine**](ivmvirtualmachine.md) .<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Definisce una rete virtuale.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Definisce una raccolta di oggetti [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Definisce l'oggetto applicazione Virtual PC Windows di livello superiore.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualPC**](ivmvirtualpc.md) .<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Nota per gli sviluppatori in Windows a 64 bit

Nelle edizioni di Windows a 64 bit, la libreria dei tipi per Windows Virtual PC si trova in un file binario a 64 bit (VPC.exe) nella directory% WinDir% \\ system32. Questa directory non è visibile per impostazione predefinita ai processi a 32 bit; WOW64 esegue il mapping di tutti gli accessi alla directory% WinDir% \\ system32 alla directory% windir% \\ SysWow64 per impostazione predefinita. Visual Studio è un file binario a 32 bit e pertanto non è in grado di aprire il file in questo percorso. Per generare un assembly di interoperabilità per Windows Virtual PC, usare TlbImp.exe, che viene fornita con Visual Studio e il Windows SDK. Per generare *Microsoft.VirtualPC.Interop.dll*, usare la riga di comando seguente:

**TlbImp.exe/out: * * * Microsoft.VirtualPC.Interop.dll* **/namespace: Microsoft. VirtualPC. Interop% WinDir% \\ system32 \\VPC.exe**

Altre soluzioni includono la copia di VPC.exe in una directory diversa in cui il compilatore lo trova o l'uso dello strumento OleView.exe dal Windows SDK per estrarre un file IDL dalla libreria dei tipi in VPC.exe.

 

