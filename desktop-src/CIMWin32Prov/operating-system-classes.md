---
description: La categoria Sistema operativo raggruppa le classi che rappresentano oggetti correlati al sistema operativo.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Classi del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5cbb168b2a322b5ceae8a2bd73985d14a74b4f1df227fd3e6cce384c554742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588291"
---
# <a name="operating-system-classes"></a>Classi del sistema operativo

La categoria Sistema operativo raggruppa le classi che rappresentano oggetti correlati al sistema operativo. Indicano le varie configurazioni e impostazioni che definiscono un ambiente di elaborazione. Ad esempio: configurazione di avvio, Component Object Model (COM), impostazioni dell'ambiente desktop, driver, impostazioni di sicurezza, impostazioni utente e impostazioni del Registro di sistema.

La categoria Sistema operativo è raggruppata nelle sottocategorie seguenti:

-   [COM](#com)
-   [Desktop](#desktop)
-   [Driver](#drivers)
-   [Registro eventi](#windows-event-log)
-   [File system](#file-system)
-   [Oggetti processo](#job-objects)
-   [Memoria e file di pagina](#memory-and-page-files)
-   [Audio multimediale o oggetto visivo](#multimedia-audio-or-visual)
-   [Rete](#networking)
-   [Eventi del sistema operativo](#operating-system-events)
-   [Impostazioni del sistema operativo](#operating-system-settings)
-   [Processi](#processes)
-   [Registro](#registry)
-   [Processi dell'utilità di pianificazione](#scheduler-jobs)
-   [Sicurezza](#security)
-   [Services](#services)
-   [Condivisioni](#shares)
-   [Menu Start](#start-menu)
-   [Archiviazione](#storage)
-   [Utenti](#users)
-   [Windows'attivazione del prodotto](#windows-product-activation)

## <a name="com"></a>COM

La sottocategoria COM raggruppa le classi che rappresentano le impostazioni COM e DCOM, le classi e le impostazioni dell'applicazione client.



| Classe                                                                                           | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ClassicCOMApplicationClasses**](win32-classiccomapplicationclasses.md)               | Classe di associazione<br/> Mette in relazione un'applicazione DCOM e un componente COM raggruppati sotto di essa.<br/>                                                                             |
| [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md)                                         | Classe di istanza<br/> Rappresenta le proprietà di un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ClassicCOMClassSettings**](win32-classiccomclasssettings.md)                         | Classe di associazione<br/> Mette in relazione una classe COM e le impostazioni usate per configurare le istanze della classe COM.<br/>                                                           |
| [**Win32 \_ ClientApplicationSetting**](win32-clientapplicationsetting.md)                       | Classe di associazione<br/> Mette in relazione un eseguibile e un'applicazione DCOM che contiene le opzioni di configurazione DCOM per il file eseguibile.<br/>                           |
| [**Applicazione COM Win32 \_**](win32-comapplication.md)                                           | Classe di istanza<br/> Rappresenta un'applicazione COM.<br/>                                                                                                                   |
| [**Classi \_ COMApplicationClasses Win32**](win32-comapplicationclasses.md)                             | Classe di associazione<br/> Mette in relazione un componente COM e l'applicazione COM in cui si trova.<br/>                                                                            |
| [**Win32 \_ COMApplicationSettings**](win32-comapplicationsettings.md)                           | Classe di associazione<br/> Mette in relazione un'applicazione DCOM e le relative impostazioni di configurazione.<br/>                                                                                   |
| [**Classe COM Win32 \_**](win32-comclass.md)                                                       | Classe di istanza<br/> Rappresenta le proprietà di un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ComClassAutoEmulator**](win32-comclassautoemulator.md)                               | Classe di associazione<br/> Mette in relazione una classe COM e un'altra classe COM che emula automaticamente.<br/>                                                                    |
| [**Win32 \_ ComClassEmulator**](win32-comclassemulator.md)                                       | Classe di associazione<br/> Mette in relazione due versioni di una classe COM.<br/>                                                                                                         |
| [**Win32 \_ ComponentCategory**](win32-componentcategory.md)                                     | Classe di istanza<br/> Rappresenta una categoria di componenti.<br/>                                                                                                                |
| [**Win32 \_ COMSetting**](win32-comsetting.md)                                                   | Classe di istanza<br/> Rappresenta le impostazioni associate a un componente COM o a un'applicazione COM.<br/>                                                                     |
| [**Win32 \_ DCOMApplication**](win32-dcomapplication.md)                                         | Classe di istanza<br/> Rappresenta le proprietà di un'applicazione DCOM.<br/>                                                                                                |
| [**Win32 \_ DCOMApplicationAccessAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Classe di associazione<br/> Mette in relazione [**l'istanza \_ win32 DCOMApplication**](win32-dcomapplication.md) e le identificazioni di sicurezza utente (SID) che possono accedervi.<br/> |
| [**Win32 \_ DCOMApplicationLaunchAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Classe di associazione<br/> Mette in relazione [**l'istanza \_ win32 DCOMApplication**](win32-dcomapplication.md) e i SID utente che possono avviarla.<br/>                           |
| [**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)                           | Classe di istanza<br/> Rappresenta le impostazioni di un'applicazione DCOM.<br/>                                                                                                  |
| [**Win32 \_ ImplementedCategory**](win32-implementedcategory.md)                                 | Classe di associazione<br/> Mette in relazione una categoria di componenti e la classe COM usando le relative interfacce.<br/>                                                                         |



 

## <a name="desktop"></a>Desktop

La sottocategoria Desktop raggruppa le classi che rappresentano oggetti che definiscono una configurazione desktop specifica.



| Classe                                           | Descrizione                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Desktop**](win32-desktop.md)         | Classe di istanza<br/> Rappresenta le caratteristiche comuni del desktop di un utente.<br/>                                    |
| [**Ambiente \_ Win32**](win32-environment.md) | Classe di istanza<br/> Rappresenta un'impostazione dell'ambiente o dell'ambiente di sistema in un computer che esegue Windows.<br/> |
| [**Fuso orario Win32 \_**](win32-timezone.md)       | Classe di istanza<br/> Rappresenta le informazioni sul fuso orario per un computer che esegue Windows.<br/>                   |
| [**Win32 \_ UserDesktop**](win32-userdesktop.md) | Classe di associazione<br/> Mette in relazione un account utente e le impostazioni del desktop specifiche.<br/>                   |



 

## <a name="drivers"></a>Driver

La sottocategoria Driver raggruppa le classi che rappresentano i driver di dispositivo virtuale e i driver di sistema per i servizi di base.



| Classe                                             | Descrizione                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32 \_ SystemDriver**](win32-systemdriver.md) | Classe di istanza<br/> Rappresenta il driver di sistema per un servizio di base.<br/> |



 

## <a name="file-system"></a>File system

La sottocategoria File System raggruppa le classi che rappresentano la modalità di disposta logicamente di un disco rigido. Sono inclusi il tipo di file system, la struttura di directory e il modo in cui il disco viene partizionato.



| Classe                                                                               | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CIMLogicalDeviceCIMDataFile**](win32-cimlogicaldevicecimdatafile.md)     | Classe di associazione<br/> Mette in relazione i dispositivi logici e i file di dati, che indicano i file del driver usati dal dispositivo.<br/>                                                      |
| [**Win32 \_ Directory**](win32-directory.md)                                         | Classe di istanza<br/> Rappresenta una voce di directory in un computer che esegue Windows.<br/>                                                                              |
| [**Directory \_ Win32Specification**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Classe di istanza<br/> Rappresenta il layout della directory per il prodotto.<br/>                                                                                                |
| [**Win32 \_ DiskDriveToDiskPartition**](win32-diskdrivetodiskpartition.md)           | Classe di associazione<br/> Mette in relazione un'unità disco e una partizione esistente.<br/>                                                                                         |
| [**Win32 \_ DiskPartition**](win32-diskpartition.md)                                 | Classe di istanza<br/> Rappresenta le funzionalità e la capacità di gestione di un'area partizionata di un disco fisico in un computer che esegue Windows.<br/>              |
| [**Win32 \_ DiskQuota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Classe di associazione<br/> Tiene traccia dell'utilizzo dello spazio su disco per i volumi file system NTFS.<br/>                                                                                        |
| [**Disco logico Win32 \_**](win32-logicaldisk.md)                                     | Rappresenta un'origine dati che si risolve in un dispositivo di archiviazione locale effettivo in un computer che esegue Windows.<br/>                                                            |
| [**Win32 \_ LogicalDiskRootDirectory**](win32-logicaldiskrootdirectory.md)           | Classe di associazione<br/> Mette in relazione un disco logico e la relativa struttura di directory.<br/>                                                                                          |
| [**Win32 \_ LogicalDiskToPartition**](win32-logicaldisktopartition.md)               | Classe di associazione<br/> Mette in relazione un'unità disco logica e la partizione del disco in cui si trova.<br/>                                                                           |
| [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md)                         | Rappresenta i dispositivi di archiviazione di rete mappati come dischi logici nel sistema computer che esegue Windows.<br/>                                                               |
| [**Win32 \_ OperatingSystemAutochkSetting**](/previous-versions//aa394240(v=vs.85)) | Classe di associazione<br/> Rappresenta l'associazione [**tra un'istanza \_ CIM ManagedSystemElement**](cim-managedsystemelement.md) e le impostazioni definite per l'istanza.<br/> |
| [**Win32 \_ QuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Classe di istanza<br/> Contiene informazioni sulle impostazioni per le quote disco in un volume.<br/>                                                                                       |
| [**File di collegamento Win32 \_**](win32-shortcutfile.md)                                   | Classe di istanza<br/> Rappresenta i file che sono collegamenti ad altri file, directory e comandi.<br/>                                                                  |
| [**Sottodirectory \_ Win32**](win32-subdirectory.md)                                   | Classe di associazione<br/> Mette in relazione una directory (cartella) e una delle relative sottodirectory (sottocartelle).<br/>                                                                     |
| [**Win32 \_ SystemPartitions**](win32-systempartitions.md)                           | Classe di associazione<br/> Mette in relazione un sistema di computer e una partizione del disco in tale sistema.<br/>                                                                               |
| [**Win32 \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Classe di istanza<br/> Rappresenta un'area di archiviazione su un disco rigido.<br/>                                                                                                   |
| [**Win32 \_ VolumeQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Classe di associazione<br/> Mette in relazione un volume con le impostazioni della quota per volume.<br/>                                                                                           |
| [**Win32 \_ VolumeQuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Classe di associazione<br/> Mette in relazione le impostazioni della quota disco con un volume del disco specifico.<br/>                                                                                     |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Classe di associazione<br/> Correla le quote per utente ai volumi abilitati per la quota.<br/>                                                                                            |



 

## <a name="job-objects"></a>Oggetti processo

La sottocategoria Oggetti processo raggruppa le classi che rappresentano le classi che forniscono i mezzi per instrumentare gli oggetti processo denominati. Non è possibile instrumentare un oggetto processo senza nome.



| Classe                                                                               | Descrizione                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccolta \_ Win32Statistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Classe di associazione<br/> Mette in relazione una raccolta di elementi di sistema gestiti e la classe che rappresenta informazioni statistiche sulla raccolta.<br/>                               |
| [**Win32 \_ LUID**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Classe di istanza<br/> Rappresenta un identificatore univoco locale (LUID)<br/>                                                                                                         |
| [**Win32 \_ LUIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Classe di istanza<br/> Rappresenta un LUID e i relativi attributi.<br/>                                                                                                                 |
| [**Win32 \_ NamedJobObject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Classe di istanza<br/> Rappresenta un oggetto kernel utilizzato per raggruppare i processi per controllare la durata e le risorse dei processi all'interno dell'oggetto processo.<br/> |
| [**Win32 \_ NamedJobObjectActgInfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Classe di istanza<br/> Rappresenta le informazioni di accounting di I/O per un oggetto processo.<br/>                                                                                           |
| [**Win32 \_ NamedJobObjectLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Classe di istanza<br/> Rappresenta un'associazione tra un oggetto processo e le impostazioni di limite dell'oggetto processo.<br/>                                                                     |
| [**Win32 \_ NamedJobObjectLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Classe di istanza<br/> Rappresenta le impostazioni dei limiti per un oggetto processo.<br/>                                                                                                       |
| [**Win32 \_ NamedJobObjectProcess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Classe di istanza<br/> Mette in relazione un oggetto processo e il processo contenuto nell'oggetto processo.<br/>                                                                                     |
| [**Win32 \_ NamedJobObjectSecLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Classe di istanza<br/> Mette in relazione un oggetto processo e le impostazioni del limite di sicurezza dell'oggetto processo.<br/>                                                                                      |
| [**Win32 \_ NamedJobObjectSecLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Classe di istanza<br/> Rappresenta le impostazioni del limite di sicurezza per un oggetto processo.<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Classe di istanza<br/> Rappresenta un'associazione tra un oggetto processo e la classe di informazioni di accounting di I/O dell'oggetto processo.<br/>                                                   |
| [**\_SID Win32andAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Classe di istanza<br/> Rappresenta un ID di sicurezza (SID) e i relativi attributi.<br/>                                                                                            |
| [**TokenGroup Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | classe di evento<br/> Rappresenta informazioni sui SID di gruppo in un token di accesso.<br/>                                                                                          |
| [**Token \_ Win32Privileges**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | classe di evento<br/> Rappresenta informazioni su un set di privilegi per un token di accesso.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>File di memoria e di pagina

La sottocategoria Memory and Page files raggruppa le classi che rappresentano le impostazioni di configurazione del file di pagina.



| Classe                                                                 | Descrizione                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ PageFile**](win32-pagefile.md)                             | Classe di istanza<br/> Rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un Windows sistema.<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Classe di associazione<br/> Correla le impostazioni iniziali di un file di pagina e lo stato di tali impostazioni durante il normale utilizzo.<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Classe di istanza<br/> Rappresenta le impostazioni di un file di pagina.<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Classe di istanza<br/> Rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un computer che esegue Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Audio multimediale o oggetto visivo

La classe nella sottocategoria Audio multimediale o Oggetto visivo rappresenta le proprietà del codec audio o video installato nel computer.



| Classe                                       | Descrizione                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CodecFile**](win32-codecfile.md) | Classe di istanza<br/> Rappresenta il codec audio o video installato nel computer.<br/> |



 

## <a name="networking"></a>Rete

La sottocategoria Rete raggruppa le classi che rappresentano le connessioni di rete, i client di rete e le impostazioni di connessione di rete, ad esempio il protocollo utilizzato.



| Classe                                                                            | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Classe di associazione<br/> Correla la route IP4 corrente alla tabella di route IP persistente.<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Classe di istanza<br/> Rappresenta route IP persistenti.<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Classe di istanza<br/> Rappresenta le informazioni che regolano il routing dei pacchetti di dati di rete.<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | classe di evento<br/> Rappresenta gli eventi di modifica della route IP.<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Classe di istanza<br/> Rappresenta un client di rete in un computer che esegue Windows.<br/>                           |
| [**Connessione di rete Win32 \_**](win32-networkconnection.md)                      | Classe di istanza<br/> Rappresenta una connessione di rete attiva in un Windows virtuale.<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Classe di istanza<br/> Rappresenta un protocollo e le relative caratteristiche di rete in un computer che esegue Windows.<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Classe di istanza<br/> Rappresenta un Windows NT dominio.<br/>                                                             |
| [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Classe di istanza<br/> Rappresenta i valori restituiti dal **comando ping** standard.<br/>                            |
| [**Win32 \_ ProtocolBinding**](win32-protocolbinding.md)                          | Classe di associazione<br/> Mette in relazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.<br/>                    |



 

## <a name="operating-system-events"></a>Eventi sistema operativo

La sottocategoria Eventi del sistema operativo raggruppa le classi che rappresentano gli eventi nel sistema operativo correlati a processi, thread e arresto del sistema.



| Classe                                                                                 | Descrizione                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | classe di evento<br/> Rappresenta gli eventi di arresto del computer.<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | classe di evento<br/> Rappresenta gli eventi correlati a un computer.<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | classe di evento<br/> Rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer.<br/>               |
| [**Modulo \_ Win32LoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | classe di evento<br/> Indica che un processo ha caricato un nuovo modulo.<br/>                                                                                      |
| [**Win32 \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | classe di evento<br/> Evento di base per gli eventi del modulo.<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | classe di evento<br/> Indica che è stato avviato un nuovo processo.<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | classe di evento<br/> Indica che un processo è stato terminato.<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | classe di evento<br/> Evento di base per gli eventi del processo.<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | classe di evento<br/> Indica che l'elenco di dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata).<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | classe di evento<br/> Classe di base per tutti gli eventi di traccia di sistema, incluse le tracce di moduli, processi e thread.<br/>                                                  |
| [**Win32 \_ ThreadStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | classe di evento<br/> Indica che è stato avviato un nuovo thread.<br/>                                                                                                    |
| [**Thread \_ Win32StopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | classe di evento<br/> Indica che un thread è stato arrestato.<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | classe di evento<br/> Classe di evento di base per gli eventi del thread.<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | classe di evento<br/> Rappresenta un evento di unità mappato alla rete risultante dall'aggiunta di una lettera di unità di rete o di un'unità montata nel sistema del computer.<br/> |



 

## <a name="operating-system-settings"></a>Impostazioni del sistema operativo

Il sistema operativo Impostazioni sottocategoria raggruppa le classi che rappresentano il sistema operativo e le relative impostazioni.



| Classe                                                                                       | Descrizione                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BootConfiguration**](win32-bootconfiguration.md)                                 | Classe di istanza<br/> Rappresenta la configurazione di avvio di un computer che esegue Windows.<br/>                                                                       |
| [**Win32 \_ ComputerSystem**](win32-computersystem.md)                                       | Classe di istanza<br/> Rappresenta un sistema operativo in un ambiente Windows locale.<br/>                                                                              |
| [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md)                     | Classe di associazione<br/> Mette in relazione un sistema di computer e un processore in esecuzione in tale sistema.<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Classe di istanza<br/> Rappresenta un prodotto.<br/>                                                                                                                         |
| [**Win32 \_ DependentService**](win32-dependentservice.md)                                   | Classe di associazione<br/> Mette in relazione due servizi di base interdipendenti.<br/>                                                                                                  |
| [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Classe di istanza<br/> Rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.<br/>                                                                     |
| [**Win32 \_ LoadOrderGroupServiceDependencies**](win32-loadordergroupservicedependencies.md) | Classe di istanza<br/> Rappresenta un'associazione tra un servizio di base e un gruppo di ordini di carico da cui il servizio dipende per avviare l'esecuzione.<br/>                         |
| [**Win32 \_ LoadOrderGroupServiceMembers**](win32-loadordergroupservicemembers.md)           | Classe di associazione<br/> Mette in relazione un gruppo di ordini di carico e un servizio di base.<br/>                                                                                             |
| [**Sistema operativo \_ Win32**](win32-operatingsystem.md)                                     | Classe di istanza<br/> Rappresenta un sistema operativo installato in un computer che esegue Windows.<br/>                                                                |
| [**Win32 \_ OperatingSystemQFE**](win32-operatingsystemqfe.md)                               | Classe di associazione<br/> Mette in relazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentato in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Classe di istanza<br/> Rappresenta i tipi di informazioni che verranno raccolte dalla memoria in caso di errore del sistema operativo.<br/>                                        |
| [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)                             | Classe di istanza<br/> Rappresenta gli aggiornamenti correzione rapida engineering (QFE) a livello di sistema applicati al sistema operativo corrente.<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Classe di istanza<br/> Rappresenta un comando che viene eseguito automaticamente quando un utente accede al sistema del computer.<br/>                                                       |
| [**Win32 \_ SystemBootConfiguration**](win32-systembootconfiguration.md)                     | Classe di associazione<br/> Mette in relazione un sistema di computer e la relativa configurazione di avvio.<br/>                                                                                      |
| [**Sistema \_ Win32Desktop**](win32-systemdesktop.md)                                         | Classe di associazione<br/> Mette in relazione un sistema di computer e la relativa configurazione desktop.<br/>                                                                                   |
| [**Sistema \_ Win32Dispositori**](win32-systemdevices.md)                                         | Classe di associazione<br/> Mette in relazione un sistema di computer e un dispositivo logico installato in tale sistema.<br/>                                                                   |
| [**Win32 \_ SystemLoadOrderGroups**](win32-systemloadordergroups.md)                         | Classe di associazione<br/> Mette in relazione un sistema informatico e un gruppo di ordini di carico.<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Classe di associazione<br/> Mette in relazione una connessione di rete e il sistema di computer in cui si trova.<br/>                                                                  |
| [**Win32 \_ SystemOperatingSystem**](win32-systemoperatingsystem.md)                         | Classe di associazione<br/> Mette in relazione un sistema informatico e il relativo sistema operativo.<br/>                                                                                        |
| [**Processi di sistema \_ Win32**](win32-systemprocesses.md)                                     | Classe di associazione <br/> Mette in relazione un sistema di computer e un processo in esecuzione in tale sistema.<br/>                                                                           |
| [**\_SystemProgramGroup Win32**](win32-systemprogramgroups.md)                             | Classe di associazione<br/> Mette in relazione un sistema informatico e un gruppo di programmi logici.<br/>                                                                                     |
| [**Risorse di sistema \_ Win32**](win32-systemresources.md)                                     | Classe di associazione<br/> Mette in relazione una risorsa di sistema e il computer in cui risiede.<br/>                                                                           |
| [**Servizi di sistema \_ Win32**](win32-systemservices.md)                                       | Classe di associazione<br/> Mette in relazione un sistema informatico e un programma di servizio esistente nel sistema.<br/>                                                                 |
| [**Win32 \_ SystemSetting**](win32-systemsetting.md)                                         | Classe di associazione<br/> Mette in relazione un sistema informatico e un'impostazione generale su tale sistema.<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Classe di associazione<br/> Mette in relazione un sistema di computer e un driver di sistema in esecuzione in tale sistema.<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Classe di associazione<br/> Mette in relazione un sistema informatico e un fuso orario.<br/>                                                                                                 |
| [**Win32 \_ SystemUsers**](win32-systemusers.md)                                             | Classe di associazione<br/> Mette in relazione un sistema di computer e un account utente in tale sistema.<br/>                                                                               |



 

## <a name="processes"></a>Processi

La sottocategoria Processi raggruppa le classi che rappresentano processi e thread di sistema.



| Classe                                                 | Descrizione                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Processo \_ Win32**](win32-process.md)               | Classe di istanza<br/> Rappresenta una sequenza di eventi in un computer che esegue Windows.<br/>      |
| [**Processo \_ Win32Avvio**](win32-processstartup.md) | Classe di istanza<br/> Rappresenta la configurazione di avvio di un computer che esegue Windows.<br/> |
| [**Win32 \_ Thread**](win32-thread.md)                 | Classe di istanza<br/> Rappresenta un thread di esecuzione.<br/>                                          |



 

## <a name="registry"></a>Registro

La classe nella sottocategoria Registro di sistema rappresenta il contenuto del Windows registro.



| Classe                                     | Descrizione                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Registro \_ Win32**](win32-registry.md) | Classe di istanza<br/> Rappresenta il Registro di sistema in un computer che esegue Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Processi dell'Utilità di pianificazione

La sottocategoria Processi dell'utilità di pianificazione raggruppa le classi che rappresentano le impostazioni dei processi pianificati.



| Classe                                                | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Classe astratta<br/> Rappresenta un'istanza nel tempo come secondi, minuti, giorno della settimana e così via.<br/>                                                                                                                                        |
| [**Processo pianificato \_ Win32**](win32-scheduledjob.md)    | Classe di istanza<br/> Rappresenta un processo pianificato usando il Windows di pianificazione.<br/>                                                                                                                                                                   |
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Classe di istanza<br/> Rappresenta un punto nel tempo restituito [**come oggetti Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) risultati da una query. La **proprietà Hour** viene restituita come ora locale in un orologio di 24 ore.<br/>                                |
| [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Classe di istanza<br/> Rappresenta un punto nel tempo restituito come [**oggetti WIN32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) risultati da una query. La **proprietà Hour** viene restituita come ora UTC (Coordinated Universal Time) in un orologio di 24 ore.<br/> |



 

## <a name="security"></a>Sicurezza

La sottocategoria Sicurezza raggruppa le classi che rappresentano le impostazioni di sicurezza del sistema.



| Classe                                                                               | Descrizione                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Id account \_ Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Classe di associazione<br/> Mette in relazione un'istanza dell'account di sicurezza con un'istanza del descrittore di sicurezza.<br/>                                             |
| [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Classe di istanza<br/> Rappresenta una voce di controllo di accesso (ACE, Access Control Entry).<br/>                                                                               |
| [**Win32 \_ LogicalFileAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di un file o di una directory e di un membro del relativo elenco di controllo di accesso discrezionale (DACL).<br/> |
| [**File logico \_ Win32Auditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di un file o di una directory di un membro del relativo elenco di controllo di accesso di sistema (SACL).<br/>            |
| [**Win32 \_ LogicalFileGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di un file o di una directory e del relativo gruppo.<br/>                                                  |
| [**Win32 \_ LogicalFileOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di un file o di una directory e del relativo proprietario.<br/>                                                  |
| [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Classe di istanza<br/> Rappresenta le impostazioni di sicurezza per un file logico.<br/>                                                                        |
| [**Win32 \_ LogicalShareAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di una condivisione e di un membro dell'elenco DACL.<br/>                                                 |
| [**Condivisione logica \_ Win32Auditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di una condivisione e di un membro del relativo SACL.<br/>                                                 |
| [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Classe di istanza<br/> Rappresenta le impostazioni di sicurezza per un file logico.<br/>                                                                        |
| [**Win32 \_ PrivilegesStatus**](win32-privilegesstatus.md)                           | Classe di istanza<br/> Rappresenta informazioni sui privilegi necessari per completare un'operazione.<br/>                                          |
| [**Descrittore di sicurezza Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Classe di istanza<br/> Rappresenta una rappresentazione strutturale di [**un \_ DESCRITTORE DI SICUREZZA.**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)<br/>                   |
| [**Win32 \_ SecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Classe di istanza<br/> Rappresenta le impostazioni di sicurezza per un elemento gestito.<br/>                                                                     |
| [**Win32 \_ SecuritySettingAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Classe di istanza<br/> Rappresenta i diritti concessi e negati a un fiduciare per un determinato oggetto .<br/>                                               |
| [**Impostazione della sicurezza \_ Win32Auditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Classe di istanza<br/> Rappresenta il controllo per un trustee specificato in un oggetto specificato.<br/>                                                          |
| [**Win32 \_ SecuritySettingGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Classe di associazione<br/> Mette in relazione la sicurezza di un oggetto e del relativo gruppo.<br/>                                                                     |
| [**Win32 \_ SecuritySettingOfLogicalFile**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Classe di istanza<br/> Rappresenta le impostazioni di sicurezza di un file o di un oggetto directory.<br/>                                                             |
| [**Win32 \_ SecuritySettingOfLogicalShare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Classe di istanza<br/> Rappresenta le impostazioni di sicurezza di un oggetto condiviso.<br/>                                                                        |
| [**Win32 \_ SecuritySettingOfObject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Classe di associazione<br/> Mette in relazione un oggetto con le relative impostazioni di sicurezza.<br/>                                                                          |
| [**Win32 \_ SecuritySettingOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Classe di associazione<br/> Mette in relazione le impostazioni di sicurezza di un oggetto e del relativo proprietario.<br/>                                                            |
| [**Win32 \_ SID**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Classe di istanza<br/> Rappresenta un SID arbitrario.<br/>                                                                                            |
| [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Classe di istanza<br/> Rappresenta un fiduciare.<br/>                                                                                                   |



 

## <a name="services"></a>Servizi

La sottocategoria Servizi raggruppa le classi che rappresentano servizi e servizi di base.



| Classe                                           | Descrizione                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BaseService**](win32-baseservice.md) | Classe di istanza<br/> Rappresenta gli oggetti eseguibili installati in un database del Registro di sistema gestito da Gestione controllo servizi.<br/> |
| [**Servizio \_ Win32**](win32-service.md)         | Classe di istanza<br/> Rappresenta un servizio in un computer che esegue Windows.<br/>                                                         |



 

## <a name="shares"></a>Condivisioni

La sottocategoria Condivisioni raggruppa le classi che rappresentano i dettagli delle risorse condivise, ad esempio stampanti e cartelle.



| Classe                                                       | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nodo DFS Win32 \_**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Classe di associazione<br/> Rappresenta un nodo radice o nodo di giunzione di un'istanza distribuita file system (DFS) basata su dominio.<br/>                                                           |
| [**Win32 \_ DFSNodeTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Classe di associazione<br/> Rappresenta la relazione di un nodo DFS con una delle relative destinazioni.<br/>                                                                                             |
| [**Win32 \_ DFSTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Classe di associazione<br/> Rappresenta la destinazione di un nodo DFS.<br/>                                                                                                                         |
| [**Win32 \_ ServerConnection**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Classe di istanza<br/> Rappresenta le connessioni effettuate da un computer remoto a una risorsa condivisa nel computer locale.<br/>                                                              |
| [**Sessione server \_ Win32**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Classe di istanza<br/> Rappresenta le sessioni stabilite con il computer locale dagli utenti in un computer remoto.<br/>                                                             |
| [**Condivisione connessione Win32 \_**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Classe di associazione<br/> Mette in relazione una risorsa condivisa nel computer e la connessione effettuata alla risorsa condivisa.<br/>                                                                    |
| [**Condivisione stampanti Win32 \_**](win32-printershare.md)           | Classe di associazione<br/> Mette in relazione una stampante locale e la condivisione che la rappresenta quando viene visualizzata in rete.<br/>                                                                     |
| [**Win32 \_ SessionConnection**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Classe di associazione<br/> Rappresenta un'associazione tra una sessione stabilita con il server locale da un utente in un computer remoto e le connessioni che dipendono dalla sessione.<br/> |
| [**Win32 \_ SessionProcess**](win32-sessionprocess.md)       | Classe di associazione<br/> Rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.<br/>                                                            |
| [**Win32 \_ ShareToDirectory**](win32-sharetodirectory.md)   | Classe di associazione<br/> Mette in relazione una risorsa condivisa nel sistema del computer e la directory a cui è mappata.<br/>                                                                    |
| [**Condivisione \_ Win32**](win32-share.md)                         | Classe di istanza<br/> Rappresenta una risorsa condivisa in un computer che esegue Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menu Start

La sottocategoria Menu Start raggruppa le classi che rappresentano i gruppi di programmi.



| Classe                                                                                   | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LogicalProgramGroup**](win32-logicalprogramgroup.md)                         | Classe di istanza<br/> Rappresenta un gruppo di programmi in un computer che esegue Windows.<br/>                                                                    |
| [**Win32 \_ LogicalProgramGroupDirectory**](win32-logicalprogramgroupdirectory.md)       | Classe di associazione<br/> Mette in relazione i gruppi di programmi logici (raggruppamenti nel menu Start) e le directory di file in cui sono archiviati.<br/>                 |
| [**Win32 \_ LogicalProgramGroupItem**](win32-logicalprogramgroupitem.md)                 | Classe di istanza<br/> Rappresenta un elemento contenuto in **un'istanza \_ di Win32 ProgramGroup,** che non è un'altra **istanza di \_ Win32 ProgramGroup.**<br/> |
| [**Win32 \_ LogicalProgramGroupItemDataFile**](win32-logicalprogramgroupitemdatafile.md) | Classe di associazione<br/> Mette in relazione gli elementi del gruppo di menu Start e i file in cui sono archiviati.<br/>                                       |
| [**Win32 \_ ProgramGroupContents**](win32-programgroupcontents.md)                       | Classe di associazione<br/> Mette in relazione un ordine dei gruppi di programmi e un singolo gruppo di programmi o un singolo elemento in esso contenuto.<br/>                                           |
| [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)                           | Classe di istanza<br/> Rappresenta un raggruppamento logico di programmi nel menu **Start** \| **Programmi dell'utente.**<br/>                                               |



 

## <a name="storage"></a>Archiviazione

La sottocategoria Users raggruppa le classi che rappresentano le informazioni di archiviazione.



| Classe                                                                   | Descrizione                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ShadowBy**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Classe di associazione<br/> Rappresenta l'associazione tra una copia shadow e il provider che crea la copia shadow.<br/>      |
| [**Win32 \_ ShadowContext**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Classe di associazione<br/> Specifica la modalità di creazione, query o eliminazione di una copia shadow.<br/>                                   |
| [**Win32 \_ ShadowCopy**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Classe di istanza<br/> Rappresenta una copia duplicata del volume originale in un momento precedente.<br/>                                  |
| [**Win32 \_ ShadowDiffVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Classe di associazione<br/> Rappresenta un'associazione tra un provider di copie shadow e un volume di archiviazione.<br/>                       |
| [**Win32 \_ ShadowFor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Classe di associazione<br/> Rappresenta un'associazione tra una copia shadow e il volume per cui viene creata la copia shadow.<br/> |
| [**Win32 \_ ShadowOn**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Classe di associazione<br/> Rappresenta un'associazione tra una copia shadow e la posizione in cui vengono scritti i dati differenziali.<br/>          |
| [**Win32 \_ ShadowProvider**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Classe di associazione<br/> Rappresenta un componente che crea e rappresenta copie shadow del volume.<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Classe di associazione<br/> Rappresenta un'associazione tra una copia shadow e la posizione in cui vengono scritti i dati differenziali.<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Classe di associazione<br/> Rappresenta un'associazione tra un provider di copie shadow e un volume supportato.<br/>                    |
| [**Win32 \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Classe di istanza<br/> Rappresenta un'area di archiviazione su un disco rigido.<br/>                                                           |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Classe di associazione<br/> Rappresenta un volume per le impostazioni della quota per volume.<br/>                                                |



 

## <a name="users"></a>Utenti

La sottocategoria Utenti raggruppa le classi che rappresentano le informazioni sull'account utente, ad esempio i dettagli di appartenenza ai gruppi.



| Classe                                                                 | Descrizione                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Account**](win32-account.md)                               | Classe di istanza<br/> Rappresenta informazioni sugli account utente e gli account di gruppo noti al computer che esegue Windows.<br/> |
| [**Gruppo \_ Win32**](win32-group.md)                                   | Classe di istanza<br/> Rappresenta i dati relativi a un account di gruppo.<br/>                                                                      |
| [**Win32 \_ GroupInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Classe di associazione<br/> Identifica gli account di gruppo associati a un Windows NT dominio.<br/>                                       |
| [**Win32 \_ GroupUser**](win32-groupuser.md)                           | Classe di associazione<br/> Mette in relazione un gruppo e un account membro di tale gruppo.<br/>                                           |
| [**Win32 \_ LogonSession**](win32-logonsession.md)                     | Classe di istanza<br/> Descrive la sessione o le sessioni di accesso associate a un utente connesso a Windows.<br/>                        |
| [**Win32 \_ LogonSessionMappedDisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Classe di istanza<br/> Rappresenta i dischi logici mappati associati alla sessione.<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Classe di istanza<br/> Rappresenta le informazioni di accesso alla rete di un utente specifico in un computer che esegue Windows.<br/>           |
| [**Account di sistema \_ Win32**](win32-systemaccount.md)                   | Classe di istanza<br/> Rappresenta un account di sistema.<br/>                                                                                |
| [**Account utente \_ Win32**](win32-useraccount.md)                       | Classe di istanza<br/> Rappresenta informazioni su un account utente in un computer che esegue Windows.<br/>                           |
| [**Win32 \_ UserInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Classe di associazione<br/> Mette in relazione un account utente e un Windows NT dominio.<br/>                                                          |



 

## <a name="windows-event-log"></a>Registro eventi di Windows

La Windows sottocategoria registro eventi raggruppa le classi che rappresentano eventi, voci del registro eventi, impostazioni di configurazione del registro eventi e così via.



| Classe                                                         | Descrizione                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Classe di istanza<br/> Rappresenta i dati archiviati in un Windows di log eventi.<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Classe di istanza<br/> Rappresenta Windows eventi.<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Classe di associazione<br/> Mette in relazione le istanze [**di Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Classe di associazione<br/> Mette in relazione le [**istanze delle classi \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**\_ NTEventlogFile Win32.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Classe di associazione<br/> Mette in relazione le [**istanze di Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) [**e Win32 \_ UserAccount**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Windows Attivazione del prodotto

Windows L'attivazione del prodotto (WPA) è una tecnologia antipiracy per ridurre la copia casuale del software.



| Classe                                                                                                               | Descrizione                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Computer \_ Win32SystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Classe di associazione<br/> Mette in relazione le istanze [**di \_ ComputerSystem Win32**](win32-computersystem.md) [**e \_ WindowsProductActivation Win32.**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))<br/> |
| [**Win32 \_ Proxy**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Classe di istanza<br/> Contiene proprietà e metodi per eseguire query e configurare una connessione Internet correlata a WPA.<br/>                                                                |
| [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Classe di istanza<br/> Contiene proprietà e metodi correlati a WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

