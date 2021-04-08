---
description: La categoria hardware del computer System raggruppa le classi che rappresentano gli oggetti correlati all'hardware. Gli esempi includono dispositivi di input, dischi rigidi, schede di espansione, dispositivi video, dispositivi di rete e alimentazione del sistema.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Classi hardware del sistema del computer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966150"
---
# <a name="computer-system-hardware-classes"></a>Classi hardware del sistema del computer

La categoria hardware del computer System raggruppa le classi che rappresentano gli oggetti correlati all'hardware. Gli esempi includono dispositivi di input, dischi rigidi, schede di espansione, dispositivi video, dispositivi di rete e alimentazione del sistema.

-   [Classi del dispositivo di raffreddamento](#cooling-device-classes)
-   [Classi del dispositivo di input](#input-device-classes)
-   [Classi di archiviazione di massa](#mass-storage-classes)
-   [Classi di porte, controller e schede madri](#motherboard-controller-and-port-classes)
-   [Classi di dispositivi di rete](#networking-device-classes)
-   [Classi Power](#power-classes)
-   [Classi di stampa](#printing-classes)
-   [Classi di telefonia](#telephony-classes)
-   [Classi video e monitor](#video-and-monitor-classes)
-   [Argomenti correlati](#related-topics)

## <a name="cooling-device-classes"></a>Classi del dispositivo di raffreddamento

La sottocategoria dispositivi di raffreddamento raggruppa le classi che rappresentano ventilatori instrumentati, sonde di temperatura e dispositivi frigoriferi.



| Classe                                                     | Descrizione                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**\_Ventola Win32**](win32-fan.md)                           | Rappresenta le proprietà di un dispositivo ventola nel computer.           |
| [**\_HeatPipe Win32**](win32-heatpipe.md)                 | Rappresenta le proprietà di un dispositivo di raffreddamento della pipe di calore.                    |
| [**\_Refrigerazione Win32**](win32-refrigeration.md)       | Rappresenta le proprietà di un dispositivo di raffreddamento.                        |
| [**\_TemperatureProbe Win32**](win32-temperatureprobe.md) | Rappresenta le proprietà di un sensore di temperatura (termometro elettronico). |



 

## <a name="input-device-classes"></a>Classi del dispositivo di input

La sottocategoria dispositivi di input raggruppa le classi che rappresentano le tastiere e i dispositivi di puntamento.



| Classe                                                 | Descrizione                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**\_Tastiera Win32**](win32-keyboard.md)             | Rappresenta una tastiera installata in un computer su cui è in esecuzione Windows.                                               |
| [**\_PointingDevice Win32**](win32-pointingdevice.md) | Rappresenta un dispositivo di input utilizzato per puntare e selezionare le aree nella visualizzazione di un sistema di computer che esegue Windows. |



 

## <a name="mass-storage-classes"></a>Classi di archiviazione di massa

Le classi della sottocategoria archiviazione di massa rappresentano dispositivi di archiviazione quali unità disco rigido, unità CD-ROM e unità nastro.



| Classe                                                     | Descrizione                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_AutochkSetting Win32**](win32-autochksetting.md)     | Rappresenta le impostazioni per l'operazione di verifica autocontrollo di un disco.                               |
| [**\_CDROMDrive Win32**](win32-cdromdrive.md)             | Rappresenta un'unità CD-ROM in un computer in cui è in esecuzione Windows.                              |
| [**\_DiskDrive Win32**](win32-diskdrive.md)               | Rappresenta un'unità disco fisica come visualizzato da un computer che esegue il sistema operativo Windows. |
| [**\_FloppyDrive Win32**](win32-floppydrive.md)           | Gestisce le funzionalità di un'unità disco floppy.                                             |
| [**\_PhysicalMedia Win32**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Rappresenta qualsiasi tipo di documentazione o supporto di archiviazione.                                      |
| [**\_TapeDrive Win32**](win32-tapedrive.md)               | Rappresenta un'unità nastro in un computer in cui è in esecuzione Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Classi di porte, controller e schede madri

La scheda madre, i controller e la sottocategoria delle porte raggruppa le classi che rappresentano i dispositivi di sistema. Gli esempi includono memoria di sistema, memoria cache e controller.



| Classe                                                                       | Descrizione                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_1394Controller Win32**](win32-1394controller.md)                       | Rappresenta le funzionalità e la gestione di un controller 1394.<br/>                                                                                                                                               |
| [**\_1394ControllerDevice Win32**](win32-1394controllerdevice.md)           | Mette in correlazione il controller Serial Bus (IEEE 1394 FireWire) ad alta velocità e l'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) connessa.<br/>                                                            |
| [**\_AllocatedResource Win32**](win32-allocatedresource.md)                 | Mette in correlazione un dispositivo logico a una risorsa di sistema.<br/>                                                                                                                                                                 |
| [**\_AssociatedProcessorMemory Win32**](win32-associatedprocessormemory.md) | Mette in correlazione un processore e la relativa memoria cache.<br/>                                                                                                                                                                      |
| [**\_Battiscopa Win32**](win32-baseboard.md)                                 | Rappresenta un battiscopa (noto anche come scheda madre o scheda di sistema).<br/>                                                                                                                                          |
| [**\_BIOS Win32**](win32-bios.md)                                           | Rappresenta gli attributi del BIOS (Basic Input o output Services) del computer installato nel computer.<br/>                                                                                   |
| [**\_Bus Win32**](win32-bus.md)                                             | Rappresenta un bus fisico come visto da un sistema operativo Windows.<br/>                                                                                                                                               |
| [**\_CacheMemory Win32**](win32-cachememory.md)                             | Rappresenta la memoria cache (interna ed esterna) in un sistema di computer.<br/>                                                                                                                                          |
| [**\_ControllerHasHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Rappresenta gli hub downstream dal controller USB (Universal Serial Bus).<br/>                                                                                                                                 |
| [**\_DeviceBus Win32**](win32-devicebus.md)                                 | Mette in correlazione un bus di sistema e un dispositivo logico utilizzando il bus.<br/>                                                                                                                                                       |
| [**\_DeviceMemoryAddress Win32**](win32-devicememoryaddress.md)             | Rappresenta un indirizzo di memoria del dispositivo in un sistema Windows.<br/>                                                                                                                                                        |
| [**\_DeviceSettings Win32**](win32-devicesettings.md)                       | Mette in correlazione un dispositivo logico e un'impostazione che può essere applicata.<br/>                                                                                                                                              |
| [**\_DMAChannel Win32**](win32-dmachannel.md)                               | Rappresenta un canale di accesso diretto alla memoria (DMA) in un sistema di computer che esegue Windows.<br/>                                                                                                                          |
| [**\_FloppyController Win32**](win32-floppycontroller.md)                   | Rappresenta le funzionalità e la capacità di gestione di un controller di unità disco floppy.<br/>                                                                                                                         |
| [**\_IDECONTROLLER Win32**](win32-idecontroller.md)                         | Rappresenta le funzionalità di un dispositivo controller IDE (Integrated Drive Electronics).<br/>                                                                                                                        |
| [**\_IDEControllerDevice Win32**](win32-idecontrollerdevice.md)             | Classe Association che mette in correlazione un controller IDE e il dispositivo logico.<br/>                                                                                                                                       |
| [**\_InfraredDevice Win32**](win32-infrareddevice.md)                       | Rappresenta le funzionalità e la gestione di un dispositivo a infrarossi.<br/>                                                                                                                                              |
| [**\_IRQResource Win32**](win32-irqresource.md)                             | Rappresenta un numero di riga di richiesta di interrupt (IRQ) in un computer Windows.<br/>                                                                                                                                |
| [**\_MemoryArray Win32**](win32-memoryarray.md)                             | Rappresenta le proprietà della matrice di memoria di sistema del computer e degli indirizzi mappati.<br/>                                                                                                                            |
| [**\_MemoryArrayLocation Win32**](win32-memoryarraylocation.md)             | Mette in correlazione una matrice di memoria logica e la matrice di memoria fisica su cui esiste.<br/>                                                                                                                             |
| [**\_MemoryDevice Win32**](win32-memorydevice.md)                           | Rappresenta le proprietà di un dispositivo di memoria di un computer insieme ai relativi indirizzi mappati associati.<br/>                                                                                                     |
| [**\_MemoryDeviceArray Win32**](win32-memorydevicearray.md)                 | Mette in correlazione un dispositivo di memoria e la matrice di memoria in cui risiede.<br/>                                                                                                                                              |
| [**\_MemoryDeviceLocation Win32**](win32-memorydevicelocation.md)           | Classe Association che mette in correlazione un dispositivo di memoria e la memoria fisica in cui è presente.<br/>                                                                                                                     |
| [**\_MotherboardDevice Win32**](win32-motherboarddevice.md)                 | Rappresenta un dispositivo che contiene i componenti centrali del computer in cui è in esecuzione Windows.<br/>                                                                                                               |
| [**\_OnBoardDevice Win32**](win32-onboarddevice.md)                         | Rappresenta i dispositivi Adapter comuni incorporati nella scheda madre (scheda di sistema).<br/>                                                                                                                                   |
| [**\_ParallelPort Win32**](win32-parallelport.md)                           | Rappresenta le proprietà di una porta parallela in un computer che esegue Windows.<br/>                                                                                                                             |
| [**\_PCMCIAController Win32**](win32-pcmciacontroller.md)                   | Gestisce le funzionalità di un dispositivo controller scheda di interfaccia della scheda di memoria (PCMCIA) personal computer.<br/>                                                                                                      |
| [**\_PhysicalMemory Win32**](win32-physicalmemory.md)                       | Rappresenta un dispositivo di memoria fisica che si trova in un computer come disponibile per il sistema operativo.<br/>                                                                                                                |
| [**\_PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md)             | Rappresenta i dettagli relativi alla memoria fisica del sistema del computer.<br/>                                                                                                                                                |
| [**\_PhysicalMemoryLocation Win32**](win32-physicalmemorylocation.md)       | Mette in correlazione una matrice di memoria fisica e la relativa memoria fisica.<br/>                                                                                                                                                   |
| [**\_PNPAllocatedResource Win32**](win32-pnpallocatedresource.md)           | Rappresenta un'associazione tra dispositivi logici e risorse di sistema.<br/>                                                                                                                                        |
| [**\_PNPDevice Win32**](win32-pnpdevice.md)                                 | Mette in correlazione un dispositivo (noto a Configuration Manager come PNPEntity) e la funzione che esegue.<br/>                                                                                                                |
| [**\_PNPEntity Win32**](win32-pnpentity.md)                                 | Rappresenta le proprietà di un dispositivo Plug and Play.<br/>                                                                                                                                                           |
| [**\_PortConnector Win32**](win32-portconnector.md)                         | Rappresenta le porte di connessione fisiche, ad esempio DB-25 pin maschio, Centronics e PS/2.<br/>                                                                                                                            |
| [**\_PortResource Win32**](win32-portresource.md)                           | Rappresenta una porta di I/O in un computer che esegue Windows.<br/>                                                                                                                                                   |
| [**\_Processore Win32**](win32-processor.md)                                 | Rappresenta un dispositivo in grado di interpretare una sequenza di istruzioni del computer in un computer in cui è in esecuzione Windows.<br/>                                                                                           |
| [**\_Controller SCSI Win32**](win32-scsicontroller.md)                       | Rappresenta un controller di Small Computer System Interface (SCSI) in un sistema di computer che esegue Windows.<br/>                                                                                                           |
| [**\_SCSIControllerDevice Win32**](win32-scsicontrollerdevice.md)           | Mette in correlazione un controller SCSI e il dispositivo logico (unità disco) connesso.<br/>                                                                                                                                 |
| [**\_SerialPort Win32**](win32-serialport.md)                               | Rappresenta una porta seriale in un sistema di computer che esegue Windows.<br/>                                                                                                                                                 |
| [**\_SerialPortConfiguration Win32**](win32-serialportconfiguration.md)     | Rappresenta le impostazioni per la trasmissione dei dati su una porta seriale di Windows.<br/>                                                                                                                                        |
| [**\_SerialPortSetting Win32**](win32-serialportsetting.md)                 | Mette in correlazione una porta seriale e le relative impostazioni di configurazione.<br/>                                                                                                                                                          |
| [**\_SMBIOSMemory Win32**](win32-smbiosmemory.md)                           | Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.<br/>                                                                                                                                  |
| [**\_SoundDevice Win32**](win32-sounddevice.md)                             | Rappresenta le proprietà di un dispositivo audio in un computer in cui è in esecuzione Windows.<br/>                                                                                                                              |
| [**\_SystemBIOS Win32**](win32-systembios.md)                               | Mette in correlazione un sistema di computer (inclusi dati quali le proprietà di avvio, i fusi orari, le configurazioni di avvio o le password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).<br/> |
| [**\_SystemDriverPNPEntity Win32**](win32-systemdriverpnpentity.md)         | Mette in correlazione un dispositivo Plug and Play sul computer Windows e il driver che supporta il dispositivo Plug and Play.<br/>                                                                                           |
| [**\_SystemEnclosure Win32**](win32-systemenclosure.md)                     | Rappresenta le proprietà associate a un'enclosure di sistema fisica.<br/>                                                                                                                                         |
| [**\_SystemMemoryResource Win32**](win32-systemmemoryresource.md)           | Rappresenta una risorsa di memoria di sistema in un sistema Windows.<br/>                                                                                                                                                       |
| [**\_SystemSlot Win32**](win32-systemslot.md)                               | Rappresenta punti di connessione fisici, tra cui porte, slot della scheda madre e periferiche e punti di connessione proprietari.<br/>                                                                                  |
| [**\_USBController Win32**](win32-usbcontroller.md)                         | Gestisce le funzionalità di un controller USB (Universal Serial Bus).<br/>                                                                                                                                           |
| [**\_USBControllerDevice Win32**](win32-usbcontrollerdevice.md)             | Mette in correlazione un controller USB e le istanze [**\_ LogicalDevice CIM**](cim-logicaldevice.md) connesse.<br/>                                                                                                    |
| [**\_USBHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Rappresenta le caratteristiche di gestione di un hub USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Classi di dispositivi di rete

La sottocategoria dispositivi di rete raggruppa le classi che rappresentano il controller di interfaccia di rete, le relative configurazioni e le relative impostazioni.



| Classe                                                                           | Descrizione                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NetworkAdapter Win32**](win32-networkadapter.md)                           | Rappresenta una scheda di rete in un sistema di computer che esegue Windows.<br/>                                                                                                                                          |
| [**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) | Rappresenta gli attributi e i comportamenti di una scheda di rete. Non è garantito che la classe sia supportata dopo la ratifica della specifica della rete CIM DMTF (Distributed Management Task Force).<br/> |
| [**\_NetworkAdapterSetting Win32**](win32-networkadaptersetting.md)             | Mette in correlazione una scheda di rete e le relative impostazioni di configurazione.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Classi Power

Power SubCategory raggruppa le classi che rappresentano alimentatori, batterie ed eventi correlati a questi dispositivi.



| Classe                                                             | Descrizione                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_Batteria Win32**](win32-battery.md)                           | Rappresenta una batteria connessa al sistema del computer.<br/>                                     |
| [**\_CurrentProbe Win32**](win32-currentprobe.md)                 | Rappresenta le proprietà di un sensore di monitoraggio corrente (amperometro).<br/>                        |
| [**\_PortableBattery Win32**](win32-portablebattery.md)           | Rappresenta le proprietà di una batteria portatile, ad esempio una utilizzata per un computer notebook.<br/> |
| [**\_PowerManagementEvent Win32**](win32-powermanagementevent.md) | Rappresenta gli eventi di risparmio energia derivanti da modifiche allo stato di alimentazione.<br/>                     |
| [**\_VoltageProbe Win32**](win32-voltageprobe.md)                 | Rappresenta le proprietà di un sensore di tensione (voltmetro elettronico).<br/>                      |



 

## <a name="printing-classes"></a>Classi di stampa

La sottocategoria stampa raggruppa le classi che rappresentano stampanti, configurazioni di stampanti e processi di stampa.



| Classe                                                             | Descrizione                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DriverForDevice Win32**](win32-driverfordevice.md)           | Mette in correlazione una stampante a un driver della stampante.<br/>                                                                                        |
| [**\_Stampante Win32**](win32-printer.md)                           | Rappresenta un dispositivo connesso a un sistema di computer che esegue Windows in grado di riprodurre un'immagine visiva su un supporto.<br/> |
| [**\_PrinterConfiguration Win32**](win32-printerconfiguration.md) | Definisce la configurazione per un dispositivo stampante.<br/>                                                                               |
| [**\_PrinterController Win32**](win32-printercontroller.md)       | Mette in correlazione una stampante e il dispositivo locale a cui è connessa la stampante.<br/>                                                     |
| [**\_PrinterDriver Win32**](win32-printerdriver.md)               | Rappresenta i driver per un'istanza di [**\_ stampante Win32**](win32-printer.md) .<br/>                                                |
| [**\_PrinterDriverDll Win32**](win32-printerdriverdll.md)         | Mette in correlazione una stampante locale e il relativo file di driver (non il driver stesso).<br/>                                                          |
| [**\_PrinterSetting Win32**](win32-printersetting.md)             | Mette in correlazione una stampante e le relative impostazioni di configurazione.<br/>                                                                             |
| [**\_PrintJob Win32**](win32-printjob.md)                         | Rappresenta un processo di stampa generato da un'applicazione basata su Windows.<br/>                                                              |
| [**\_TCPIPPrinterPort Win32**](win32-tcpipprinterport.md)         | Rappresenta un punto di accesso del servizio TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Classi di telefonia

La sottocategoria telefonia raggruppa le classi che rappresentano i dispositivi modem "Plain Old Phone" e le relative connessioni seriali associate.



| Classe                                                               | Descrizione                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_POTSModem Win32**](win32-potsmodem.md)                         | Rappresenta i servizi e le caratteristiche di un modem del servizio telefonico (POTS) Plain Old in un computer che esegue Windows.<br/> |
| [**\_POTSModemToSerialPort Win32**](win32-potsmodemtoserialport.md) | Mette in correlazione un modem e la porta seriale utilizzata dal modem.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Classi video e monitor

La sottocategoria video e monitoraggi raggruppa le classi che rappresentano i monitoraggi, le schede video e le impostazioni associate.



| Classe                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DesktopMonitor Win32**](win32-desktopmonitor.md)                                 | Rappresenta il tipo di monitoraggio o dispositivo di visualizzazione collegato al sistema del computer.<br/>                                                                                                                                                                                                                                                                                       |
| [**\_DisplayControllerConfiguration Win32**](win32-displaycontrollerconfiguration.md) | Rappresenta le informazioni di configurazione della scheda video di un sistema di computer che esegue Windows. Questa classe è obsoleta. Al posto di questa classe, usare le proprietà nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [CIM \_ VideoControllerResolution](cim-videocontrollerresolution.md) .<br/> |
| [**\_VideoController Win32**](win32-videocontroller.md)                               | Rappresenta le funzionalità e la capacità di gestione del controller video in un sistema di computer che esegue Windows.<br/>                                                                                                                                                                                                                                                       |
| [**\_VideoSettings Win32**](win32-videosettings.md)                                   | Mette in correlazione un controller video e le impostazioni video a cui è possibile applicare.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

