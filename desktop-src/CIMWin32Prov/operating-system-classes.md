---
description: La categoria del sistema operativo raggruppa le classi che rappresentano gli oggetti correlati al sistema operativo.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Classi del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f47df8a949e3ac07bf2099ea708d496bed87298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305288"
---
# <a name="operating-system-classes"></a>Classi del sistema operativo

La categoria del sistema operativo raggruppa le classi che rappresentano gli oggetti correlati al sistema operativo. Indicano le varie configurazioni e impostazioni che definiscono un ambiente di elaborazione. Esempi di configurazione di avvio, Component Object Model (COM), impostazioni dell'ambiente desktop, driver, impostazioni di sicurezza, impostazioni utente e impostazioni del registro di sistema.

La categoria del sistema operativo è raggruppata nelle sottocategorie seguenti:

-   [COM](#com)
-   [Desktop](#desktop)
-   [Driver](#drivers)
-   [Registro eventi](#windows-event-log)
-   [File system](#file-system)
-   [Oggetti processo](#job-objects)
-   [File di memoria e di paging](#memory-and-page-files)
-   [Audio multimediale o oggetti visivi](#multimedia-audio-or-visual)
-   [Funzionalità di rete](#networking)
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
-   [Attivazione del prodotto Windows](#windows-product-activation)

## <a name="com"></a>COM

La sottocategoria COM raggruppa le classi che rappresentano le impostazioni di COM e DCOM, le classi e le impostazioni dell'applicazione client.



| Classe                                                                                           | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ClassicCOMApplicationClasses Win32**](win32-classiccomapplicationclasses.md)               | Classe Association<br/> Mette in correlazione un'applicazione DCOM e un componente COM raggruppati al suo interno.<br/>                                                                             |
| [**\_ClassicCOMClass Win32**](win32-classiccomclass.md)                                         | Classe dell'istanza<br/> Rappresenta le proprietà di un componente COM.<br/>                                                                                                   |
| [**\_ClassicCOMClassSettings Win32**](win32-classiccomclasssettings.md)                         | Classe Association<br/> Mette in correlazione una classe COM e le impostazioni utilizzate per configurare le istanze della classe COM.<br/>                                                           |
| [**\_ClientApplicationSetting Win32**](win32-clientapplicationsetting.md)                       | Classe Association<br/> Mette in correlazione un eseguibile e un'applicazione DCOM che contiene le opzioni di configurazione DCOM per il file eseguibile.<br/>                           |
| [**ComApplicazione Win32 \_**](win32-comapplication.md)                                           | Classe dell'istanza<br/> Rappresenta un'applicazione COM.<br/>                                                                                                                   |
| [**\_COMApplicationClasses Win32**](win32-comapplicationclasses.md)                             | Classe Association<br/> Mette in correlazione un componente COM e l'applicazione COM in cui risiede.<br/>                                                                            |
| [**\_COMApplicationSettings Win32**](win32-comapplicationsettings.md)                           | Classe Association<br/> Mette in correlazione un'applicazione DCOM e le relative impostazioni di configurazione.<br/>                                                                                   |
| [**Comclasse Win32 \_**](win32-comclass.md)                                                       | Classe dell'istanza<br/> Rappresenta le proprietà di un componente COM.<br/>                                                                                                   |
| [**\_ComClassAutoEmulator Win32**](win32-comclassautoemulator.md)                               | Classe Association<br/> Mette in correlazione una classe COM e un'altra classe COM che emula automaticamente.<br/>                                                                    |
| [**\_ComClassEmulator Win32**](win32-comclassemulator.md)                                       | Classe Association<br/> Mette in relazione due versioni di una classe COM.<br/>                                                                                                         |
| [**\_ComponentCategory Win32**](win32-componentcategory.md)                                     | Classe dell'istanza<br/> Rappresenta una categoria di componenti.<br/>                                                                                                                |
| [**Comimpostazioni Win32 \_**](win32-comsetting.md)                                                   | Classe dell'istanza<br/> Rappresenta le impostazioni associate a un componente COM o a un'applicazione COM.<br/>                                                                     |
| [**\_DCOMApplication Win32**](win32-dcomapplication.md)                                         | Classe dell'istanza<br/> Rappresenta le proprietà di un'applicazione DCOM.<br/>                                                                                                |
| [**\_DCOMApplicationAccessAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Classe Association<br/> Mette in correlazione l'istanza di [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) e gli identificatori di sicurezza (SID) utente che possono accedervi.<br/> |
| [**\_DCOMApplicationLaunchAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Classe Association<br/> Mette in correlazione l'istanza [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) e i SID utente che possono avviarlo.<br/>                           |
| [**\_DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md)                           | Classe dell'istanza<br/> Rappresenta le impostazioni di un'applicazione DCOM.<br/>                                                                                                  |
| [**\_ImplementedCategory Win32**](win32-implementedcategory.md)                                 | Classe Association<br/> Mette in correlazione una categoria di componenti e la classe COM usando le relative interfacce.<br/>                                                                         |



 

## <a name="desktop"></a>Desktop

La sottocategoria desktop raggruppa le classi che rappresentano oggetti che definiscono una configurazione desktop specifica.



| Classe                                           | Descrizione                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Desktop Win32**](win32-desktop.md)         | Classe dell'istanza<br/> Rappresenta le caratteristiche comuni del desktop di un utente.<br/>                                    |
| [**\_Ambiente Win32**](win32-environment.md) | Classe dell'istanza<br/> Rappresenta un'impostazione dell'ambiente o dell'ambiente di sistema in un computer che esegue Windows.<br/> |
| [**\_Fuso orario Win32**](win32-timezone.md)       | Classe dell'istanza<br/> Rappresenta le informazioni sul fuso orario per un computer che esegue Windows.<br/>                   |
| [**\_UserDesktop Win32**](win32-userdesktop.md) | Classe Association<br/> Mette in correlazione un account utente e le impostazioni desktop specifiche.<br/>                   |



 

## <a name="drivers"></a>Driver

La sottocategoria drivers raggruppa le classi che rappresentano i driver di dispositivo virtuale e i driver di sistema per i servizi di base.



| Classe                                             | Descrizione                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_SystemDriver Win32**](win32-systemdriver.md) | Classe dell'istanza<br/> Rappresenta il driver di sistema per un servizio di base.<br/> |



 

## <a name="file-system"></a>File system

La sottocategoria file System raggruppa le classi che rappresentano il modo in cui un disco rigido viene disposto logicamente. Sono inclusi il tipo di file system utilizzati, la struttura di directory e la modalità di partizionamento del disco.



| Classe                                                                               | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CIMLogicalDeviceCIMDataFile Win32**](win32-cimlogicaldevicecimdatafile.md)     | Classe Association<br/> Mette in relazione i dispositivi logici e i file di dati, indicando i file del driver usati dal dispositivo.<br/>                                                      |
| [**\_Directory Win32**](win32-directory.md)                                         | Classe dell'istanza<br/> Rappresenta una voce di directory in un computer in cui è in esecuzione Windows.<br/>                                                                              |
| [**\_DirectorySpecification Win32**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Classe dell'istanza<br/> Rappresenta il layout di directory per il prodotto.<br/>                                                                                                |
| [**\_DiskDriveToDiskPartition Win32**](win32-diskdrivetodiskpartition.md)           | Classe Association<br/> Mette in correlazione un'unità disco e una partizione esistente.<br/>                                                                                         |
| [**\_DiskPartition Win32**](win32-diskpartition.md)                                 | Classe dell'istanza<br/> Rappresenta le funzionalità e la capacità di gestione di un'area partizionata di un disco fisico in un sistema di computer che esegue Windows.<br/>              |
| [**\_DiskQuota Win32**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Classe Association<br/> Tiene traccia dell'utilizzo dello spazio su disco per i volumi file system NTFS.<br/>                                                                                        |
| [**\_Disco logico Win32**](win32-logicaldisk.md)                                     | Rappresenta un'origine dati che viene risolta in un dispositivo di archiviazione locale effettivo in un computer in cui è in esecuzione Windows.<br/>                                                            |
| [**\_LogicalDiskRootDirectory Win32**](win32-logicaldiskrootdirectory.md)           | Classe Association<br/> Mette in correlazione un disco logico e la relativa struttura di directory.<br/>                                                                                          |
| [**\_LogicalDiskToPartition Win32**](win32-logicaldisktopartition.md)               | Classe Association<br/> Mette in relazione un'unità disco logica e la partizione del disco su cui si trova.<br/>                                                                           |
| [**\_MappedLogicalDisk Win32**](win32-mappedlogicaldisk.md)                         | Rappresenta i dispositivi di archiviazione di rete mappati come dischi logici nel computer in cui è in esecuzione Windows.<br/>                                                               |
| [**\_OperatingSystemAutochkSetting Win32**](/previous-versions//aa394240(v=vs.85)) | Classe Association<br/> Rappresenta l'associazione tra un'istanza di [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) e le impostazioni definite.<br/> |
| [**\_QuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Classe dell'istanza<br/> Contiene informazioni sull'impostazione per le quote disco in un volume.<br/>                                                                                       |
| [**\_ShortcutFile Win32**](win32-shortcutfile.md)                                   | Classe dell'istanza<br/> Rappresenta i file che sono collegamenti ad altri file, directory e comandi.<br/>                                                                  |
| [**Sottodirectory Win32 \_**](win32-subdirectory.md)                                   | Classe Association<br/> Mette in correlazione una directory (cartella) e una delle relative sottodirectory (sottocartelle).<br/>                                                                     |
| [**\_SystemPartitions Win32**](win32-systempartitions.md)                           | Classe Association<br/> Mette in correlazione un sistema del computer e una partizione del disco nel sistema.<br/>                                                                               |
| [**\_Volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Classe dell'istanza<br/> Rappresenta un'area di archiviazione su un disco rigido.<br/>                                                                                                   |
| [**\_VolumeQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Classe Association<br/> Mette in relazione un volume con le impostazioni della quota per volume.<br/>                                                                                           |
| [**\_VolumeQuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Classe Association<br/> Correla le impostazioni della quota del disco con un volume del disco specifico.<br/>                                                                                     |
| [**\_VolumeUserQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Classe Association<br/> Relazione tra le quote utente e i volumi abilitati per la quota.<br/>                                                                                            |



 

## <a name="job-objects"></a>Oggetti processo

La sottocategoria oggetti processo raggruppa le classi che rappresentano le classi che forniscono i mezzi per instrumentare oggetti processo denominati. Un oggetto processo senza nome non può essere instrumentato.



| Classe                                                                               | Descrizione                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CollectionStatistics Win32**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Classe Association<br/> Mette in correlazione una raccolta di elementi di sistema gestita e la classe che rappresenta le informazioni statistiche sulla raccolta.<br/>                               |
| [**\_LUID Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Classe dell'istanza<br/> Rappresenta un identificatore univoco locale (LUID)<br/>                                                                                                         |
| [**\_LUIDandAttributes Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Classe dell'istanza<br/> Rappresenta un LUID e i relativi attributi.<br/>                                                                                                                 |
| [**\_NamedJobObject Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Classe dell'istanza<br/> Rappresenta un oggetto kernel utilizzato per raggruppare i processi per controllare la durata e le risorse dei processi all'interno dell'oggetto processo.<br/> |
| [**\_NamedJobObjectActgInfo Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Classe dell'istanza<br/> Rappresenta le informazioni di accounting di I/O per un oggetto processo.<br/>                                                                                           |
| [**\_NamedJobObjectLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Classe dell'istanza<br/> Rappresenta un'associazione tra un oggetto processo e le impostazioni del limite dell'oggetto processo.<br/>                                                                     |
| [**\_NamedJobObjectLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Classe dell'istanza<br/> Rappresenta le impostazioni limite per un oggetto processo.<br/>                                                                                                       |
| [**\_NamedJobObjectProcess Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Classe dell'istanza<br/> Mette in correlazione un oggetto processo e il processo contenuto nell'oggetto processo.<br/>                                                                                     |
| [**\_NamedJobObjectSecLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Classe dell'istanza<br/> Mette in correlazione un oggetto processo e le impostazioni dei limiti di sicurezza dell'oggetto processo.<br/>                                                                                      |
| [**\_NamedJobObjectSecLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Classe dell'istanza<br/> Rappresenta le impostazioni dei limiti di sicurezza per un oggetto processo.<br/>                                                                                              |
| [**\_NamedJobObjectStatistics Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Classe dell'istanza<br/> Rappresenta un'associazione tra un oggetto processo e la classe di informazioni di contabilità di I/O dell'oggetto processo.<br/>                                                   |
| [**\_SIDandAttributes Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Classe dell'istanza<br/> Rappresenta un ID di sicurezza (SID) e i relativi attributi.<br/>                                                                                            |
| [**\_TokenGroups Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | classe di evento<br/> Rappresenta le informazioni sui SID di gruppo in un token di accesso.<br/>                                                                                          |
| [**\_TokenPrivileges Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | classe di evento<br/> Rappresenta le informazioni su un set di privilegi per un token di accesso.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>File di memoria e di paging

La sottocategoria file di memoria e di paging raggruppa le classi che rappresentano le impostazioni di configurazione del file di paging.



| Classe                                                                 | Descrizione                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Pagefile Win32**](win32-pagefile.md)                             | Classe dell'istanza<br/> Rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Windows.<br/>                  |
| [**\_PageFileElementSetting Win32**](win32-pagefileelementsetting.md) | Classe Association<br/> Mette in correlazione le impostazioni iniziali di un file di paging e lo stato di tali impostazioni durante il normale utilizzo.<br/>        |
| [**\_PageFileSetting Win32**](win32-pagefilesetting.md)               | Classe dell'istanza<br/> Rappresenta le impostazioni di un file di paging.<br/>                                                                  |
| [**\_PageFileUsage Win32**](win32-pagefileusage.md)                   | Classe dell'istanza<br/> Rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un computer in cui è in esecuzione Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Audio multimediale o oggetti visivi

La classe nell'audio multimediale o nella sottocategoria Visual rappresenta le proprietà del codec audio o video installato nel computer.



| Classe                                       | Descrizione                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Codecfile Win32 \_**](win32-codecfile.md) | Classe dell'istanza<br/> Rappresenta il codec audio o video installato nel computer.<br/> |



 

## <a name="networking"></a>Rete

La sottocategoria rete raggruppa le classi che rappresentano le connessioni di rete, i client di rete e le impostazioni di connessione di rete, ad esempio il protocollo usato.



| Classe                                                                            | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_ActiveRoute Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Classe Association<br/> Mette in correlazione la route IP4 corrente alla tabella di route IP permanente.<br/>                           |
| [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Classe dell'istanza<br/> Rappresenta route IP permanente.<br/>                                                             |
| [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Classe dell'istanza<br/> Rappresenta le informazioni che governano il routing dei pacchetti di dati di rete.<br/>                    |
| [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | classe di evento<br/> Rappresenta gli eventi di modifica della route IP.<br/>                                                             |
| [**\_Networkclient Win32**](win32-networkclient.md)                              | Classe dell'istanza<br/> Rappresenta un client di rete in un sistema di computer che esegue Windows.<br/>                           |
| [**\_NetworkConnection Win32**](win32-networkconnection.md)                      | Classe dell'istanza<br/> Rappresenta una connessione di rete attiva in un ambiente Windows.<br/>                           |
| [**\_NetworkProtocol Win32**](win32-networkprotocol.md)                          | Classe dell'istanza<br/> Rappresenta un protocollo e le relative caratteristiche di rete in un sistema di computer che esegue Windows.<br/> |
| [**\_NTDOMAIN Win32**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Classe dell'istanza<br/> Rappresenta un dominio di Windows NT.<br/>                                                             |
| [**\_PingStatus Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Classe dell'istanza<br/> Rappresenta i valori restituiti dal comando **ping** standard.<br/>                            |
| [**\_Protocollo di protocollo Win32**](win32-protocolbinding.md)                          | Classe Association<br/> Mette in correlazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.<br/>                    |



 

## <a name="operating-system-events"></a>Eventi sistema operativo

La sottocategoria eventi del sistema operativo raggruppa le classi che rappresentano gli eventi del sistema operativo correlati a processi, thread e arresto del sistema.



| Classe                                                                                 | Descrizione                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ComputerShutdownEvent Win32**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | classe di evento<br/> Rappresenta gli eventi di arresto del computer.<br/>                                                                                                   |
| [**\_ComputerSystemEvent Win32**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | classe di evento<br/> Rappresenta gli eventi correlati a un sistema di computer.<br/>                                                                                        |
| [**\_DeviceChangeEvent Win32**](win32-devicechangeevent.md)                           | classe di evento<br/> Rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer.<br/>               |
| [**\_ModuleLoadTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | classe di evento<br/> Indica che un processo ha caricato un nuovo modulo.<br/>                                                                                      |
| [**\_ModuleTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | classe di evento<br/> Evento di base per gli eventi del modulo.<br/>                                                                                                          |
| [**\_ProcessStartTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | classe di evento<br/> Indica che è stato avviato un nuovo processo.<br/>                                                                                              |
| [**\_ProcessStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | classe di evento<br/> Indica che un processo è stato terminato.<br/>                                                                                               |
| [**\_ProcessTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | classe di evento<br/> Evento di base per gli eventi di processo.<br/>                                                                                                         |
| [**\_SystemConfigurationChangeEvent Win32**](win32-systemconfigurationchangeevent.md) | classe di evento<br/> Indica che l'elenco dei dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata).<br/>    |
| [**\_SystemTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | classe di evento<br/> Classe di base per tutti gli eventi di traccia di sistema, incluse le tracce del modulo, del processo e del thread.<br/>                                                  |
| [**\_ThreadStartTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | classe di evento<br/> Indica che è stato avviato un nuovo thread.<br/>                                                                                                    |
| [**\_ThreadStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | classe di evento<br/> Indica che un thread è stato arrestato.<br/>                                                                                                   |
| [**\_ThreadTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | classe di evento<br/> Classe di evento di base per gli eventi del thread.<br/>                                                                                                    |
| [**\_VolumeChangeEvent Win32**](win32-volumechangeevent.md)                           | classe di evento<br/> Rappresenta un evento di unità mappato alla rete risultante dall'aggiunta di una lettera di unità di rete o di un'unità montata nel computer.<br/> |



 

## <a name="operating-system-settings"></a>Impostazioni del sistema operativo

La sottocategoria impostazioni sistema operativo raggruppa le classi che rappresentano il sistema operativo e le relative impostazioni.



| Classe                                                                                       | Descrizione                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BootConfiguration Win32**](win32-bootconfiguration.md)                                 | Classe dell'istanza<br/> Rappresenta la configurazione di avvio di un sistema di computer che esegue Windows.<br/>                                                                       |
| [**\_ComputerSystem Win32**](win32-computersystem.md)                                       | Classe dell'istanza<br/> Rappresenta un sistema di computer che opera in un ambiente Windows.<br/>                                                                              |
| [**\_ComputerSystemProcessor Win32**](win32-computersystemprocessor.md)                     | Classe Association<br/> Mette in correlazione un computer e un processore in esecuzione in tale sistema.<br/>                                                                          |
| [**\_ComputerSystemProduct Win32**](win32-computersystemproduct.md)                         | Classe dell'istanza<br/> Rappresenta un prodotto.<br/>                                                                                                                         |
| [**\_DependentService Win32**](win32-dependentservice.md)                                   | Classe Association<br/> Mette in relazione due servizi di base interdipendenti.<br/>                                                                                                  |
| [**\_LoadOrderGroup Win32**](win32-loadordergroup.md)                                       | Classe dell'istanza<br/> Rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.<br/>                                                                     |
| [**\_LoadOrderGroupServiceDependencies Win32**](win32-loadordergroupservicedependencies.md) | Classe dell'istanza<br/> Rappresenta un'associazione tra un servizio di base e un gruppo dell'ordine di caricamento da cui il servizio dipende per avviare l'esecuzione.<br/>                         |
| [**\_LoadOrderGroupServiceMembers Win32**](win32-loadordergroupservicemembers.md)           | Classe Association<br/> Mette in correlazione un gruppo dell'ordine di caricamento e un servizio di base.<br/>                                                                                             |
| [**\_OperatingSystem Win32**](win32-operatingsystem.md)                                     | Classe dell'istanza<br/> Rappresenta un sistema operativo installato in un computer in cui è in esecuzione Windows.<br/>                                                                |
| [**\_OperatingSystemQFE Win32**](win32-operatingsystemqfe.md)                               | Classe Association<br/> Mette in relazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentati in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).<br/> |
| [**\_OSRecoveryConfiguration Win32**](win32-osrecoveryconfiguration.md)                     | Classe dell'istanza<br/> Rappresenta i tipi di informazioni che verranno raccolte dalla memoria quando si verifica un errore nel sistema operativo.<br/>                                        |
| [**\_QuickFixEngineering Win32**](win32-quickfixengineering.md)                             | Classe dell'istanza<br/> Rappresenta il QFE (Quick Fix Engineering) o gli aggiornamenti a livello di sistema applicati al sistema operativo corrente.<br/>                         |
| [**\_StartupCommand Win32**](win32-startupcommand.md)                                       | Classe dell'istanza<br/> Rappresenta un comando che viene eseguito automaticamente quando un utente accede al computer.<br/>                                                       |
| [**\_SystemBootConfiguration Win32**](win32-systembootconfiguration.md)                     | Classe Association<br/> Mette in correlazione un sistema computer e la relativa configurazione di avvio.<br/>                                                                                      |
| [**\_SystemDesktop Win32**](win32-systemdesktop.md)                                         | Classe Association<br/> Mette in correlazione un sistema computer e la relativa configurazione desktop.<br/>                                                                                   |
| [**\_SystemDevices Win32**](win32-systemdevices.md)                                         | Classe Association<br/> Mette in correlazione un computer e un dispositivo logico installati in tale sistema.<br/>                                                                   |
| [**\_SystemLoadOrderGroups Win32**](win32-systemloadordergroups.md)                         | Classe Association<br/> Mette in correlazione un sistema di computer e un gruppo di ordini di caricamento.<br/>                                                                                          |
| [**\_SystemNetworkConnections Win32**](win32-systemnetworkconnections.md)                   | Classe Association<br/> Mette in correlazione una connessione di rete e il computer in cui risiede.<br/>                                                                  |
| [**\_SystemOperatingSystem Win32**](win32-systemoperatingsystem.md)                         | Classe Association<br/> Mette in correlazione un sistema di computer e il relativo sistema operativo.<br/>                                                                                        |
| [**\_SystemProcesses Win32**](win32-systemprocesses.md)                                     | Classe Association <br/> Mette in relazione un computer e un processo in esecuzione in tale sistema.<br/>                                                                           |
| [**\_SystemProgramGroups Win32**](win32-systemprogramgroups.md)                             | Classe Association<br/> Mette in correlazione un sistema di computer e un gruppo di programmi logici.<br/>                                                                                     |
| [**\_SystemResources Win32**](win32-systemresources.md)                                     | Classe Association<br/> Mette in relazione una risorsa di sistema e il sistema del computer in cui risiede.<br/>                                                                           |
| [**\_SystemServices Win32**](win32-systemservices.md)                                       | Classe Association<br/> Mette in correlazione un sistema del computer e un programma del servizio esistente nel sistema.<br/>                                                                 |
| [**\_SystemSetting Win32**](win32-systemsetting.md)                                         | Classe Association<br/> Mette in correlazione un sistema del computer e un'impostazione generale del sistema.<br/>                                                                            |
| [**\_SystemSystemDriver Win32**](win32-systemsystemdriver.md)                               | Classe Association<br/> Mette in correlazione un sistema di computer e un driver di sistema in esecuzione nel computer.<br/>                                                             |
| [**\_SystemTimeZone Win32**](win32-systemtimezone.md)                                       | Classe Association<br/> Mette in correlazione un sistema di computer e un fuso orario.<br/>                                                                                                 |
| [**\_SystemUsers Win32**](win32-systemusers.md)                                             | Classe Association<br/> Mette in correlazione un sistema di computer e un account utente nel sistema.<br/>                                                                               |



 

## <a name="processes"></a>Processi

La sottocategoria processi raggruppa le classi che rappresentano i processi e i thread di sistema.



| Classe                                                 | Descrizione                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_Processo Win32**](win32-process.md)               | Classe dell'istanza<br/> Rappresenta una sequenza di eventi in un sistema di computer che esegue Windows.<br/>      |
| [**\_ProcessStartup Win32**](win32-processstartup.md) | Classe dell'istanza<br/> Rappresenta la configurazione di avvio di un sistema di computer che esegue Windows.<br/> |
| [**\_Thread Win32**](win32-thread.md)                 | Classe dell'istanza<br/> Rappresenta un thread di esecuzione.<br/>                                          |



 

## <a name="registry"></a>Registro

La classe nella sottocategoria Registry rappresenta il contenuto del registro di sistema di Windows.



| Classe                                     | Descrizione                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_Registro Win32**](win32-registry.md) | Classe dell'istanza<br/> Rappresenta il registro di sistema in un computer in cui è in esecuzione Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Processi dell'Utilità di pianificazione

La sottocategoria processi dell'utilità di pianificazione raggruppa le classi che rappresentano le impostazioni del processo pianificato.



| Classe                                                | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CurrentTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Classe astratta<br/> Rappresenta un'istanza nel tempo come componente secondi, minuti, giorno della settimana e così via.<br/>                                                                                                                                        |
| [**\_ScheduledJob Win32**](win32-scheduledjob.md)    | Classe dell'istanza<br/> Rappresenta un processo pianificato utilizzando il servizio di pianificazione di Windows.<br/>                                                                                                                                                                   |
| [**\_Localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Classe dell'istanza<br/> Rappresenta un punto nel tempo restituito come [**oggetti \_ localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) che risultano da una query. La proprietà **hour** viene restituita come ora locale in un formato a 24 ore.<br/>                                |
| [**\_UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Classe dell'istanza<br/> Rappresenta un punto nel tempo restituito come oggetti [**\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) che risultano da una query. La proprietà **hour** viene restituita come ora UTC (Coordinated Universal Time) in un clock a 24 ore.<br/> |



 

## <a name="security"></a>Sicurezza

La sottocategoria sicurezza raggruppa le classi che rappresentano le impostazioni di sicurezza del sistema.



| Classe                                                                               | Descrizione                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AccountSid Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Classe Association<br/> Mette in correlazione un'istanza dell'account di sicurezza con un'istanza del descrittore di sicurezza.<br/>                                             |
| [**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Classe dell'istanza<br/> Rappresenta una voce di controllo di accesso (ACE, Access Control Entry).<br/>                                                                               |
| [**\_LogicalFileAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di un file o di una directory e un membro dell'elenco di controllo di accesso discrezionale (DACL).<br/> |
| [**\_LogicalFileAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di un file o di una directory di un membro del relativo elenco di controllo di accesso di sistema (SACL).<br/>            |
| [**\_LogicalFileGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di un file o di una directory e del relativo gruppo.<br/>                                                  |
| [**\_LogicalFileOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di un file o di una directory e del relativo proprietario.<br/>                                                  |
| [**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Classe dell'istanza<br/> Rappresenta le impostazioni di sicurezza per un file logico.<br/>                                                                        |
| [**\_LogicalShareAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di una condivisione e di un membro del relativo DACL.<br/>                                                 |
| [**\_LogicalShareAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di una condivisione e di un membro del relativo SACL.<br/>                                                 |
| [**\_LogicalShareSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Classe dell'istanza<br/> Rappresenta le impostazioni di sicurezza per un file logico.<br/>                                                                        |
| [**\_PrivilegesStatus Win32**](win32-privilegesstatus.md)                           | Classe dell'istanza<br/> Rappresenta le informazioni sui privilegi necessari per completare un'operazione.<br/>                                          |
| [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Classe dell'istanza<br/> Rappresenta una rappresentazione strutturale di un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).<br/>                   |
| [**\_SecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Classe dell'istanza<br/> Rappresenta le impostazioni di sicurezza per un elemento gestito.<br/>                                                                     |
| [**\_SecuritySettingAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Classe dell'istanza<br/> Rappresenta i diritti concessi e negati a un trustee per un oggetto specificato.<br/>                                               |
| [**\_SecuritySettingAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Classe dell'istanza<br/> Rappresenta il controllo per un determinato trustee in un oggetto specificato.<br/>                                                          |
| [**\_SecuritySettingGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Classe Association<br/> Mette in correlazione la sicurezza di un oggetto e del relativo gruppo.<br/>                                                                     |
| [**\_SecuritySettingOfLogicalFile Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Classe dell'istanza<br/> Rappresenta le impostazioni di sicurezza di un oggetto file o directory.<br/>                                                             |
| [**\_SecuritySettingOfLogicalShare Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Classe dell'istanza<br/> Rappresenta le impostazioni di sicurezza di un oggetto condiviso.<br/>                                                                        |
| [**\_SecuritySettingOfObject Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Classe Association<br/> Mette in relazione un oggetto con le relative impostazioni di sicurezza.<br/>                                                                          |
| [**\_SecuritySettingOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Classe Association<br/> Mette in correlazione le impostazioni di sicurezza di un oggetto e del relativo proprietario.<br/>                                                            |
| [**\_SID Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Classe dell'istanza<br/> Rappresenta un SID arbitrario.<br/>                                                                                            |
| [**\_Trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Classe dell'istanza<br/> Rappresenta un trustee.<br/>                                                                                                   |



 

## <a name="services"></a>Servizi

La sottocategoria Services raggruppa le classi che rappresentano servizi e servizi di base.



| Classe                                           | Descrizione                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BaseService Win32**](win32-baseservice.md) | Classe dell'istanza<br/> Rappresenta gli oggetti eseguibili installati in un database del registro di sistema gestito da Gestione controllo servizi.<br/> |
| [**\_Servizio Win32**](win32-service.md)         | Classe dell'istanza<br/> Rappresenta un servizio in un sistema di computer che esegue Windows.<br/>                                                         |



 

## <a name="shares"></a>Condivisioni

La sottocategoria shares raggruppa le classi che rappresentano i dettagli delle risorse condivise, ad esempio le stampanti e le cartelle.



| Classe                                                       | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DFSNode Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Classe Association<br/> Rappresenta un nodo radice o di giunzione di una file system distribuita basata su dominio o autonoma (DFS).<br/>                                                           |
| [**\_DFSNodeTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Classe Association<br/> Rappresenta la relazione di un nodo DFS con una delle relative destinazioni.<br/>                                                                                             |
| [**\_DFSTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Classe Association<br/> Rappresenta la destinazione di un nodo DFS.<br/>                                                                                                                         |
| [**\_ServerConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Classe dell'istanza<br/> Rappresenta le connessioni effettuate da un computer remoto a una risorsa condivisa nel computer locale.<br/>                                                              |
| [**\_ServerSession Win32**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Classe dell'istanza<br/> Rappresenta le sessioni stabilite con il computer locale dagli utenti in un computer remoto.<br/>                                                             |
| [**\_ConnectionShare Win32**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Classe Association<br/> Mette in correlazione una risorsa condivisa nel computer e la connessione effettuata alla risorsa condivisa.<br/>                                                                    |
| [**\_PrinterShare Win32**](win32-printershare.md)           | Classe Association<br/> Mette in correlazione una stampante locale e la condivisione che la rappresenta mentre viene visualizzata in una rete.<br/>                                                                     |
| [**\_SessionConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Classe Association<br/> Rappresenta un'associazione tra una sessione stabilita con il server locale da un utente in un computer remoto e le connessioni che dipendono dalla sessione.<br/> |
| [**\_SessionProcess Win32**](win32-sessionprocess.md)       | Classe Association<br/> Rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.<br/>                                                            |
| [**\_ShareToDirectory Win32**](win32-sharetodirectory.md)   | Classe Association<br/> Mette in correlazione una risorsa condivisa nel computer e la directory a cui viene mappata.<br/>                                                                    |
| [**\_Condivisione Win32**](win32-share.md)                         | Classe dell'istanza<br/> Rappresenta una risorsa condivisa in un sistema di computer che esegue Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menu Start

La sottocategoria del menu Start raggruppa le classi che rappresentano i gruppi di programmi.



| Classe                                                                                   | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_LogicalProgramGroup Win32**](win32-logicalprogramgroup.md)                         | Classe dell'istanza<br/> Rappresenta un gruppo di programmi in un computer in cui è in esecuzione Windows.<br/>                                                                    |
| [**\_LogicalProgramGroupDirectory Win32**](win32-logicalprogramgroupdirectory.md)       | Classe Association<br/> Mette in correlazione i gruppi di programmi logici (raggruppamenti nel menu Start) e le directory dei file in cui sono archiviati.<br/>                 |
| [**\_LogicalProgramGroupItem Win32**](win32-logicalprogramgroupitem.md)                 | Classe dell'istanza<br/> Rappresenta un elemento contenuto da un'istanza **Win32 \_ ProgramGroup** , che non è un'altra istanza **Win32 di \_ ProgramGroup** .<br/> |
| [**\_LogicalProgramGroupItemDataFile Win32**](win32-logicalprogramgroupitemdatafile.md) | Classe Association<br/> Mette in correlazione gli elementi del gruppo di programmi del menu Start e i file in cui sono archiviati.<br/>                                       |
| [**\_ProgramGroupContents Win32**](win32-programgroupcontents.md)                       | Classe Association<br/> Mette in correlazione un ordine del gruppo di programmi e un singolo gruppo o elemento del programma contenuto.<br/>                                           |
| [**\_ProgramGroupOrItem Win32**](win32-programgrouporitem.md)                           | Classe dell'istanza<br/> Rappresenta un raggruppamento logico di programmi nel menu **Start** \| **Programs** dell'utente.<br/>                                               |



 

## <a name="storage"></a>Archiviazione

La sottocategoria utenti raggruppa le classi che rappresentano le informazioni di archiviazione.



| Classe                                                                   | Descrizione                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ShadowBy Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Classe Association<br/> Rappresenta l'associazione tra una copia shadow e il provider che crea la copia shadow.<br/>      |
| [**\_ShadowContext Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Classe Association<br/> Specifica il modo in cui deve essere creata, sottoposta a query o eliminata una copia shadow.<br/>                                   |
| [**\_ShadowCopy Win32**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Classe dell'istanza<br/> Rappresenta una copia duplicata del volume originale in un momento precedente.<br/>                                  |
| [**\_ShadowDiffVolumeSupport Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Classe Association<br/> Rappresenta un'associazione tra un provider di copie shadow e un volume di archiviazione.<br/>                       |
| [**\_ShadowFor Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Classe Association<br/> Rappresenta un'associazione tra una copia shadow e il volume per il quale viene creata la copia shadow.<br/> |
| [**\_ShadowOn Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Classe Association<br/> Rappresenta un'associazione tra una copia shadow e la posizione in cui vengono scritti i dati differenziali.<br/>          |
| [**\_ShadowProvider Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Classe Association<br/> Rappresenta un componente che crea e rappresenta copie shadow del volume.<br/>                             |
| [**\_Shadowstorage Win32**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Classe Association<br/> Rappresenta un'associazione tra una copia shadow e la posizione in cui vengono scritti i dati differenziali.<br/>          |
| [**\_ShadowVolumeSupport Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Classe Association<br/> Rappresenta un'associazione tra un provider di copia shadow e un volume supportato.<br/>                    |
| [**\_Volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Classe dell'istanza<br/> Rappresenta un'area di archiviazione su un disco rigido.<br/>                                                           |
| [**\_VolumeUserQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Classe Association<br/> Rappresenta un volume per le impostazioni della quota per volume.<br/>                                                |



 

## <a name="users"></a>Utenti

La sottocategoria utenti raggruppa le classi che rappresentano le informazioni sull'account utente, ad esempio i dettagli sull'appartenenza ai gruppi.



| Classe                                                                 | Descrizione                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Account Win32**](win32-account.md)                               | Classe dell'istanza<br/> Rappresenta le informazioni sugli account utente e gli account di gruppo noti al sistema computer che esegue Windows.<br/> |
| [**\_Gruppo Win32**](win32-group.md)                                   | Classe dell'istanza<br/> Rappresenta i dati relativi a un account di gruppo.<br/>                                                                      |
| [**\_GroupInDomain Win32**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Classe Association<br/> Identifica gli account di gruppo associati a un dominio Windows NT.<br/>                                       |
| [**\_GroupUser Win32**](win32-groupuser.md)                           | Classe Association<br/> Mette in correlazione un gruppo e un account membro di tale gruppo.<br/>                                           |
| [**\_LogonSession Win32**](win32-logonsession.md)                     | Classe dell'istanza<br/> Descrive la sessione di accesso o le sessioni associate a un utente connesso a Windows.<br/>                        |
| [**\_LogonSessionMappedDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Classe dell'istanza<br/> Rappresenta i dischi logici mappati associati alla sessione.<br/>                                            |
| [**\_NetworkLoginProfile Win32**](win32-networkloginprofile.md)       | Classe dell'istanza<br/> Rappresenta le informazioni di accesso di rete di un utente specifico in un computer in cui è in esecuzione Windows.<br/>           |
| [**\_SystemAccount Win32**](win32-systemaccount.md)                   | Classe dell'istanza<br/> Rappresenta un account di sistema.<br/>                                                                                |
| [**\_AccountUtente Win32**](win32-useraccount.md)                       | Classe dell'istanza<br/> Rappresenta le informazioni su un account utente in un sistema di computer che esegue Windows.<br/>                           |
| [**\_UserInDomain Win32**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Classe Association<br/> Mette in correlazione un account utente e un dominio Windows NT.<br/>                                                          |



 

## <a name="windows-event-log"></a>Registro eventi di Windows

La sottocategoria Registro eventi di Windows raggruppa le classi che rappresentano gli eventi, le voci del registro eventi, le impostazioni di configurazione del registro eventi e così via.



| Classe                                                         | Descrizione                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NTEventlogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Classe dell'istanza<br/> Rappresenta i dati archiviati in un file di registro eventi di Windows.<br/>                                                                                      |
| [**\_NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Classe dell'istanza<br/> Rappresenta gli eventi di Windows.<br/>                                                                                                               |
| [**\_NTLogEventComputer Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Classe Association<br/> Mette in correlazione le istanze di [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**\_NTLogEventLog Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Classe Association<br/> Mette in correlazione le istanze delle classi Win32 [**\_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .<br/> |
| [**\_NTLogEventUser Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Classe Association<br/> Mette in correlazione le istanze di [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ AccountUtente**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Attivazione del prodotto Windows

L'attivazione del prodotto Windows è una tecnologia antipirateria che consente di ridurre la copia occasionale del software.



| Classe                                                                                                               | Descrizione                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ComputerSystemWindowsProductActivationSetting Win32**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Classe Association<br/> Mette in correlazione le istanze di [**Win32 \_ ComputerSystem**](win32-computersystem.md) e [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**\_Proxy Win32**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Classe dell'istanza<br/> Contiene proprietà e metodi per eseguire una query e configurare una connessione Internet correlata a WPA.<br/>                                                                |
| [**\_WindowsProductActivation Win32**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Classe dell'istanza<br/> Contiene proprietà e metodi correlati a WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

