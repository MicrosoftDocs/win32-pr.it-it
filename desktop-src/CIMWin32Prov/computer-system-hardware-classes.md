---
description: La categoria Hardware del sistema computer raggruppa le classi che rappresentano oggetti correlati all'hardware. Ad esempio, dispositivi di input, dischi rigidi, schede di espansione, dispositivi video, dispositivi di rete e alimentazione del sistema.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Classi hardware del sistema computer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d541071698c08510452faaf6bef0cd706dab66e5eaa77b5db121e522785c5c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420096"
---
# <a name="computer-system-hardware-classes"></a>Classi hardware del sistema computer

La categoria Hardware del sistema computer raggruppa le classi che rappresentano oggetti correlati all'hardware. Ad esempio, dispositivi di input, dischi rigidi, schede di espansione, dispositivi video, dispositivi di rete e alimentazione del sistema.

-   [Classi di dispositivi di raffreddamento](#cooling-device-classes)
-   [Classi di dispositivi di input](#input-device-classes)
-   [Classi di Archiviazione di massa](#mass-storage-classes)
-   [Classi scheda madre, controller e porta](#motherboard-controller-and-port-classes)
-   [Classi di dispositivi di rete](#networking-device-classes)
-   [Power Classes](#power-classes)
-   [Stampa di classi](#printing-classes)
-   [Classi di telefonia](#telephony-classes)
-   [Classi di video e monitoraggio](#video-and-monitor-classes)
-   [Argomenti correlati](#related-topics)

## <a name="cooling-device-classes"></a>Classi di dispositivi di raffreddamento

La sottocategoria Dispositivi di raffreddamento raggruppa le classi che rappresentano ventole instrumentabili, probe di temperatura e dispositivi di refrigerazione.



| Classe                                                     | Descrizione                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Ventola \_ Win32**](win32-fan.md)                           | Rappresenta le proprietà di un dispositivo a ventola nel computer.           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | Rappresenta le proprietà di un dispositivo di raffreddamento a pipe termica.                    |
| [**Refrigerazione Win32 \_**](win32-refrigeration.md)       | Rappresenta le proprietà di un dispositivo refrigerato.                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | Rappresenta le proprietà di un sensore di temperatura (termometro elettronico). |



 

## <a name="input-device-classes"></a>Classi di dispositivi di input

La sottocategoria Dispositivi di input raggruppa le classi che rappresentano tastiere e dispositivi di puntamento.



| Classe                                                 | Descrizione                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Tastiera \_ Win32**](win32-keyboard.md)             | Rappresenta una tastiera installata in un computer che esegue Windows.                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | Rappresenta un dispositivo di input utilizzato per puntare e selezionare aree sullo schermo di un computer che esegue Windows. |



 

## <a name="mass-storage-classes"></a>Classi di Archiviazione di massa

Le classi nella sottocategoria Archiviazione di archiviazione rappresentano dispositivi di archiviazione, ad esempio unità disco rigido, unità CD-ROM e unità nastro.



| Classe                                                     | Descrizione                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ AutochkSetting**](win32-autochksetting.md)     | Rappresenta le impostazioni per l'operazione di controllo automatico di un disco.                               |
| [**Unità \_ CDROM2 Win32**](win32-cdromdrive.md)             | Rappresenta un'unità CD-ROM in un computer che esegue Windows.                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | Rappresenta un'unità disco fisica come visualizzato da un computer che esegue il Windows operativo. |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | Gestisce le funzionalità di un'unità disco floppy.                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Rappresenta qualsiasi tipo di documentazione o supporto di archiviazione.                                      |
| [**Win32 \_ TapeDrive**](win32-tapedrive.md)               | Rappresenta un'unità nastro in un computer che esegue Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Classi scheda madre, controller e porta

La sottocategoria Scheda madre, Controller e Porte raggruppa le classi che rappresentano i dispositivi di sistema. Ad esempio, la memoria di sistema, la memoria cache e i controller.



| Classe                                                                       | Descrizione                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | Rappresenta le funzionalità e la gestione di un controller 1394.<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | Mette in relazione il controller del bus seriale ad alta velocità (IEEE 1394 Firewire) e [**l'istanza \_ CiM LogicalDevice**](cim-logicaldevice.md) connessa.<br/>                                                            |
| [**Risorsa allocata Win32 \_**](win32-allocatedresource.md)                 | Mette in relazione un dispositivo logico con una risorsa di sistema.<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | Mette in relazione un processore e la relativa memoria cache.<br/>                                                                                                                                                                      |
| [**Win32 \_ BaseBoard**](win32-baseboard.md)                                 | Rappresenta una scheda di base (nota anche come scheda madre o scheda di sistema).<br/>                                                                                                                                          |
| [**Win32 \_ BIOS**](win32-bios.md)                                           | Rappresenta gli attributi dei servizi di input o output (BIOS) di base del computer installati nel computer.<br/>                                                                                   |
| [**Win32 \_ Bus**](win32-bus.md)                                             | Rappresenta un bus fisico come visualizzato da un Windows operativo.<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | Rappresenta la memoria cache (interna ed esterna) in un computer.<br/>                                                                                                                                          |
| [**\_Controller Win32HasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Rappresenta gli hub downstream dal controller USB (Universal Serial Bus).<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | Mette in relazione un bus di sistema e un dispositivo logico usando il bus.<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | Rappresenta un indirizzo di memoria del dispositivo in Windows sistema.<br/>                                                                                                                                                        |
| [**Impostazioni dispositivo \_ Win32**](win32-devicesettings.md)                       | Mette in relazione un dispositivo logico e un'impostazione che può essere applicata.<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | Rappresenta un canale DMA (Direct Memory Access) in un computer che esegue Windows.<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | Rappresenta le funzionalità e la capacità di gestione di un controller dell'unità disco floppy.<br/>                                                                                                                         |
| [**Win32 \_ IDEController**](win32-idecontroller.md)                         | Rappresenta le funzionalità di un dispositivo controller IDE (Integrated Drive Electronics).<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | Classe di associazione che mette in relazione un controller IDE e il dispositivo logico.<br/>                                                                                                                                       |
| [**\_Win32Ufficio per dispositivi**](win32-infrareddevice.md)                       | Rappresenta le funzionalità e la gestione di un dispositivo a bluetooth.<br/>                                                                                                                                              |
| [**Risorsa \_ IRQ Win32**](win32-irqresource.md)                             | Rappresenta un numero IRQ (Interrupt Request Line) in un computer Windows computer.<br/>                                                                                                                                |
| [**Win32 \_ MemoryArray**](win32-memoryarray.md)                             | Rappresenta le proprietà della matrice di memoria del computer e degli indirizzi mappati.<br/>                                                                                                                            |
| [**Win32 \_ MemoryArrayLocation**](win32-memoryarraylocation.md)             | Mette in relazione una matrice di memoria logica e la matrice di memoria fisica in cui esiste.<br/>                                                                                                                             |
| [**Win32 \_ MemoryDevice**](win32-memorydevice.md)                           | Rappresenta le proprietà del dispositivo di memoria di un computer insieme agli indirizzi mappati associati.<br/>                                                                                                     |
| [**Win32 \_ MemoryDeviceArray**](win32-memorydevicearray.md)                 | Mette in relazione un dispositivo di memoria e la matrice di memoria in cui risiede.<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | Classe di associazione che mette in relazione un dispositivo di memoria e la memoria fisica in cui esiste.<br/>                                                                                                                     |
| [**Scheda madre \_ Win32Device**](win32-motherboarddevice.md)                 | Rappresenta un dispositivo che contiene i componenti centrali del computer che esegue Windows.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Rappresenta i dispositivi adattatore comuni incorporati nella scheda madre (scheda di sistema).<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Rappresenta le proprietà di una porta parallela in un computer che esegue Windows.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Gestisce le funzionalità di un dispositivo controller PCMCIA (Personal Computer Memory Card Interface Adapter).<br/>                                                                                                      |
| [**Memoria fisica \_ Win32**](win32-physicalmemory.md)                       | Rappresenta un dispositivo di memoria fisica che si trova in un computer come disponibile per il sistema operativo.<br/>                                                                                                                |
| [**Oggetto \_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md)             | Rappresenta i dettagli sulla memoria fisica del computer.<br/>                                                                                                                                                |
| [**Percorso fisico \_ Win32**](win32-physicalmemorylocation.md)       | Mette in relazione una matrice di memoria fisica e la relativa memoria fisica.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Rappresenta un'associazione tra dispositivi logici e risorse di sistema.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Mette in relazione un dispositivo (noto Gestione configurazione come PNPEntity) e la funzione che esegue.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Rappresenta le proprietà di un Plug and Play dispositivo.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Rappresenta le porte di connessione fisiche, ad esempio db-25 pin male, Centronics e PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Rappresenta una porta di I/O in un computer che esegue Windows.<br/>                                                                                                                                                   |
| [**Processore \_ Win32**](win32-processor.md)                                 | Rappresenta un dispositivo in grado di interpretare una sequenza di istruzioni del computer in un computer che esegue Windows.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Rappresenta un controller SCSI (Small Computer System Interface) in un computer che esegue Windows.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Mette in relazione un controller SCSI e il dispositivo logico (unità disco) connesso.<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | Rappresenta una porta seriale in un computer che esegue Windows.<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | Rappresenta le impostazioni per la trasmissione dei dati su Windows porta seriale.<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | Mette in relazione una porta seriale e le relative impostazioni di configurazione.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Rappresenta le proprietà di un dispositivo audio in un computer che esegue Windows.<br/>                                                                                                                              |
| [**Win32 \_ SystemBIOS**](win32-systembios.md)                               | Mette in relazione un sistema informatico (inclusi dati quali proprietà di avvio, fusi orari, configurazioni di avvio o password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Mette in relazione Plug and Play dispositivo nel computer Windows e il driver che supporta il Plug and Play dispositivo.<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | Rappresenta le proprietà associate a un'enclosure fisica del sistema.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Rappresenta una risorsa di memoria di sistema in un Windows sistema.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Rappresenta i punti di connessione fisici, inclusi porte, slot e periferiche della scheda madre e punti di connessione proprietari.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Gestisce le funzionalità di un controller USB (Universal Serial Bus).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Mette in relazione un controller USB e [**le istanze \_ CiM LogicalDevice**](cim-logicaldevice.md) connesse.<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Rappresenta le caratteristiche di gestione di un hub USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Classi di dispositivi di rete

La sottocategoria Dispositivi di rete raggruppa le classi che rappresentano il controller di interfaccia di rete, le relative configurazioni e le relative impostazioni.



| Classe                                                                           | Descrizione                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NetworkAdapter**](win32-networkadapter.md)                           | Rappresenta una scheda di rete in un computer che esegue Windows.<br/>                                                                                                                                          |
| [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) | Rappresenta gli attributi e i comportamenti di una scheda di rete. Non è garantito che la classe sia supportata dopo l'autorizzazione della specifica di rete CIM DMTF (Distributed Management Task Force).<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Mette in relazione una scheda di rete e le relative impostazioni di configurazione.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Power Classes

La sottocategoria Power raggruppa le classi che rappresentano alimentatori, batterie ed eventi correlati a questi dispositivi.



| Classe                                                             | Descrizione                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Batteria \_ Win32**](win32-battery.md)                           | Rappresenta una batteria connessa al computer.<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | Rappresenta le proprietà di un sensore di monitoraggio corrente (ammeter).<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Rappresenta le proprietà di una batteria portatile, ad esempio quella usata per un computer notebook.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Rappresenta gli eventi di risparmio energia risultanti da modifiche dello stato di alimentazione.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Rappresenta le proprietà di un sensore di tensione (tachimetro elettronico).<br/>                      |



 

## <a name="printing-classes"></a>Stampa di classi

La sottocategoria Stampa raggruppa le classi che rappresentano stampanti, configurazioni della stampante e processi di stampa.



| Classe                                                             | Descrizione                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Driver \_ Win32ForDevice**](win32-driverfordevice.md)           | Mette in relazione una stampante con un driver della stampante.<br/>                                                                                        |
| [**Stampante \_ Win32**](win32-printer.md)                           | Rappresenta un dispositivo connesso a un computer che esegue Windows in grado di riprodurre un'immagine visiva su un supporto.<br/> |
| [**Win32 \_ PrinterConfiguration**](win32-printerconfiguration.md) | Definisce la configurazione per una periferica di stampa.<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | Mette in relazione una stampante e il dispositivo locale a cui è connessa la stampante.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Rappresenta i driver per [**un'istanza \_ della stampante Win32.**](win32-printer.md)<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | Mette in relazione una stampante locale e il relativo file di driver (non il driver stesso).<br/>                                                          |
| [**Win32 \_ PrinterSetting**](win32-printersetting.md)             | Mette in relazione una stampante e le relative impostazioni di configurazione.<br/>                                                                             |
| [**Processo di stampa \_ Win32**](win32-printjob.md)                         | Rappresenta un processo di stampa generato da un'Windows basata sull'applicazione.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Rappresenta un punto di accesso del servizio TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Classi di telefonia

La sottocategoria Telefonia raggruppa le classi che rappresentano i dispositivi modem "plain old telephone" e le relative connessioni seriali associate.



| Classe                                                               | Descrizione                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ POTSModem**](win32-potsmodem.md)                         | Rappresenta i servizi e le caratteristiche di un modem POTS (Plain Old Telephone Service) in un computer che esegue Windows.<br/> |
| [**Win32 \_ POTSModemToSerialPort**](win32-potsmodemtoserialport.md) | Mette in relazione un modem e la porta seriale utilizzata dal modem.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Classi di video e monitoraggio

Le classi della sottocategoria Video e Monitors raggruppano le classi che rappresentano monitoraggi, schede video e le relative impostazioni associate.



| Classe                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Rappresenta il tipo di dispositivo di monitoraggio o di visualizzazione collegato al sistema del computer.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | Rappresenta le informazioni di configurazione della scheda video di un computer che esegue Windows. Questa classe è obsoleta. Al posto di questa classe, usare le proprietà nelle [**classi Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [CIM \_ VideoControllerResolution.](cim-videocontrollerresolution.md)<br/> |
| [**Win32 \_ VideoController**](win32-videocontroller.md)                               | Rappresenta le funzionalità e la capacità di gestione del controller video in un computer che esegue Windows.<br/>                                                                                                                                                                                                                                                       |
| [**Win32 \_ VideoSettings**](win32-videosettings.md)                                   | Mette in relazione un controller video e le impostazioni video che possono essere applicate.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

