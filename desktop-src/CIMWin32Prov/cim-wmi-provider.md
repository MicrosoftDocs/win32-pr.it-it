---
description: Queste classi WMI vengono dichiarate in CimWin32.mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: CIM WMI Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9a01e0771645cf6101171ce870be593181cb61d6118e627b9bf96b61994be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420336"
---
# <a name="cim-wmi-provider"></a>CIM WMI Provider

Queste classi WMI vengono dichiarate in CimWin32.mof.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**Azione \_ CIM**](cim-action.md)
</dt> <dd>

Una [**classe \_ action CIM**](cim-action.md) è un'operazione che fa parte di un processo per creare un elemento software nello stato successivo o per eliminare l'elemento software nello stato corrente.

</dd> <dt>

[**CIM \_ ActionSequence**](cim-actionsequence.md)
</dt> <dd>

L'associazione [**CIM \_ ActionSequence**](cim-actionsequence.md) definisce una serie di operazioni che passano l'elemento software (a cui fa riferimento l'associazione [**\_ CIM SoftwareElementActions)**](cim-softwareelementactions.md) allo stato successivo o rimuove l'elemento software dallo stato corrente.

</dd> <dt>

[**CIM \_ ActsAsSpare**](cim-actsasspare.md)
</dt> <dd>

[**L'associazione \_ CIM ActsAsSpare**](cim-actsasspare.md) indica quali elementi possono essere di riserva o sostituire altri elementi aggregati. Una riserva può operare in modalità "hot standby" come specificato elemento per elemento.

</dd> <dt>

[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)
</dt> <dd>

[**L'associazione CIM \_ AdjacentSlots**](cim-adjacentslots.md) descrive il layout degli slot in una scheda di scheda o scheda di hosting. Le informazioni, ad esempio la distanza tra gli slot e se sono "condivise" (se ne viene popolato uno, l'altro slot non può essere usato) vengono trasmesse come proprietà di associazione.

</dd> <dt>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)
</dt> <dd>

La [**classe CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fornisce informazioni di riepilogo sui blocchi logici indirizzabili, che si trovano nello stesso gruppo di ridondanza di archiviazione e si trovano nello stesso supporto fisico.

</dd> <dt>

[**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md)
</dt> <dd>

La [**classe CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) definisce il numero di blocchi logici indirizzabili in un singolo dispositivo di archiviazione, esclusi i blocchi logici mappati come dati di controllo. Se vengono definiti set di volumi, i blocchi logici sono contenuti all'interno di un singolo set di volumi. Si tratta di un raggruppamento alternativo per [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), quando sono necessarie solo informazioni di riepilogo o quando viene usata la configurazione automatica.

</dd> <dt>

[**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md)
</dt> <dd>

La [**classe CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.

</dd> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> <dd>

La [**classe CIM \_ AlarmDevice**](cim-alarmdevice.md) è un dispositivo di allarme che genera indicazioni udibili o visibili correlate a una situazione di problema.

</dd> <dt>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dd>

La [**classe CIM \_ AllocatedResource**](cim-allocatedresource.md) rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.

</dd> <dt>

[**CIM \_ ApplicationSystem**](cim-applicationsystem.md)
</dt> <dd>

La [**classe \_ CIM ApplicationSystem**](cim-applicationsystem.md) rappresenta un'applicazione o un sistema software che supporta una particolare funzione aziendale che può essere gestita come unità indipendente. Un sistema di questo tipo può essere scomposto nei relativi componenti funzionali usando la [**classe \_ CIM SoftwareFeature.**](cim-softwarefeature.md) Le funzionalità software per un'applicazione o un sistema software specifico si trovano usando l'associazione [**\_ CIM ApplicationSystemSoftwareFeature.**](cim-applicationsystemsoftwarefeature.md)

</dd> <dt>

[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

La [**classe CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo. Le funzionalità software possono essere incluse in prodotti diversi.

</dd> <dt>

[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)
</dt> <dd>

La [**dipendenza CIM \_ AssociatedAlarm**](cim-associatedalarm.md) associa un allarme a un dispositivo logico.

</dd> <dt>

[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)
</dt> <dd>

La [**dipendenza CIM \_ AssociatedBattery**](cim-associatedbattery.md) associa una batteria a un dispositivo logico. Usare questa associazione per modellare le singole batterie che costituiscono un alimentatore (UPS) ininterrotti.

</dd> <dt>

[**CIM \_ AssociatedCooling**](cim-associatedcooling.md)
</dt> <dd>

[**L'associazione CIM \_ AssociatedCooling**](cim-associatedcooling.md) indica quando le ventole o altri dispositivi di raffreddamento sono specifici di un dispositivo (invece di fornire raffreddamento a enclosure o cablaio).

</dd> <dt>

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> <dd>

La [**classe CIM \_ AssociateMemory**](cim-associatedmemory.md) associa la memoria installata o associata, ad esempio la memoria cache a un dispositivo logico.

</dd> <dt>

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)
</dt> <dd>

La [**classe CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associa il processore e la memoria di sistema o la cache di un processore.

</dd> <dt>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> <dd>

La [**classe CIM \_ AssociatedSensor**](cim-associatedsensor.md) associa un sensore installato a un dispositivo logico. Il sensore misura le proprietà di input e output critiche e può essere incluso nel dispositivo o installato nelle vicinanze.

</dd> <dt>

[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

La [**classe CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associa un alimentatore a un sensore corrente (amperage) che monitora la frequenza di input.

</dd> <dt>

[**CIM \_ AssociatedSupplyVoltageSensor**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Associa un alimentatore a un sensore di tensione che monitora la tensione di input.

</dd> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> <dd>

La [**classe \_ CiM BasedOn**](cim-basedon.md) rappresenta un'associazione che descrive come assemblare gli extent di archiviazione da extent di livello inferiore. Ad esempio, gli extent fisici includono extent di spazio protetto. Di conseguenza, i set di volumi vengono assemblati da uno o più extent di spazio fisico o protetto. La memoria cache può essere definita in modo indipendente e realizzata in un elemento fisico oppure può essere basata su extent di archiviazione volatili o non volatili.

</dd> <dt>

[**Batteria \_ CIM**](cim-battery.md)
</dt> <dd>

La [**classe CiM \_ Battery**](cim-battery.md) rappresenta le funzionalità e la gestione del dispositivo logico a batteria. Questa classe si applica alle batterie nei sistemi portatili e ad altre batterie interne ed esterne.

</dd> <dt>

[**CIM \_ BinarySensor**](cim-binarysensor.md)
</dt> <dd>

La [**classe CIM \_ BinarySensor**](cim-binarysensor.md) fornisce un output booleano. Le **proprietà CurrentState** e **PossibleStates** sono state aggiunte per il sensore, rendendo la sottoclasse **CIM \_ BinarySensor** non più necessaria, anche se viene mantenuta per compatibilità con le versioni precedenti. È possibile creare un sensore binario creando un'istanza di un sensore con due stati possibili.

</dd> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dd>

La [**classe \_ CIM BIOSElement**](cim-bioselement.md) rappresenta il software di basso livello caricato nell'archiviazione non volatile e usato per avviare e configurare un computer.

</dd> <dt>

[**CIM \_ BIOSFeature**](cim-biosfeature.md)
</dt> <dd>

rappresenta le funzionalità del software di basso livello utilizzato per avviare e configurare un computer.

</dd> <dt>

[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)
</dt> <dd>

La [**classe CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associa una funzionalità BIOS e i relativi elementi BIOS aggregati.

</dd> <dt>

[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)
</dt> <dd>

La [**classe CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associa un elemento BIOS e l'archiviazione non volatile in cui viene caricato.

</dd> <dt>

[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)
</dt> <dd>

La [**classe \_ CIM BootOSFromFS**](cim-bootosfromfs.md) associa il sistema operativo e i file system da cui viene caricato il sistema operativo. L'associazione è molti-a-molti; Un sistema operativo distribuito può dipendere da diversi file system per il caricamento corretto e completo.

</dd> <dt>

[**CIM \_ BootSAP**](cim-bootsap.md)
</dt> <dd>

La [**classe CIM \_ BootSAP**](cim-bootsap.md) rappresenta i punti di accesso di un servizio di avvio.

</dd> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> <dd>

La [**classe \_ CiM BootService**](cim-bootservice.md) rappresenta la funzionalità fornita da un dispositivo o da un software o da una rete per caricare un sistema operativo in un computer unitario.

</dd> <dt>

[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)
</dt> <dd>

La [**classe CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associa un servizio di avvio e i relativi punti di accesso.

</dd> <dt>

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> <dd>

La [**classe \_ CiM CacheMemory**](cim-cachememory.md) definisce le funzionalità e la gestione della memoria cache.

</dd> <dt>

[**Scheda \_ CIM**](cim-card.md)
</dt> <dd>

La [**classe CIM \_ Card**](cim-card.md) rappresenta un tipo di contenitore fisico che può essere collegato a un'altra scheda o scheda di hosting oppure è a sua volta una scheda di hosting/scheda madre in uno chassis. Questa classe include qualsiasi pacchetto in grado di trasportare segnali e fornire un punto di montaggio per i componenti fisici, ad esempio chip o altri pacchetti fisici, ad esempio altre schede.

</dd> <dt>

[**CIM \_ CardInSlot**](cim-cardinslot.md)
</dt> <dd>

La [**classe CIM \_ CardInSlot**](cim-cardinslot.md) associa una scheda di scheda al contenitore in cui viene inserita.

</dd> <dt>

[**CIM \_ CardOnCard**](cim-cardoncard.md)
</dt> <dd>

L'associazione [**\_ CIM CardOnCard**](cim-cardoncard.md) descrive le relazioni relative alle schede che possono essere collegate a schede madre/schede di base, schede di una scheda o schede che supportano moduli speciali simili a schede.

</dd> <dt>

[**CIM \_ CDROMDrive**](cim-cdromdrive.md)
</dt> <dd>

La [**classe \_ CIM CDROMDrive**](cim-cdromdrive.md) rappresenta un'unità CD-ROM nel computer.

</dd> <dt>

[**CIM \_ Chassis**](cim-chassis.md)
</dt> <dd>

La classe [**\_ CIM Chassis**](cim-chassis.md) rappresenta gli elementi fisici che racchiudno altri elementi e forniscono funzionalità definibili, ad esempio un desktop, un nodo di elaborazione, un gruppo di protezione dei dati, un disco o un nastro o una combinazione di questi elementi.

</dd> <dt>

[**CIM \_ ChassisInRack**](cim-chassisinrack.md)
</dt> <dd>

[**L'associazione CIM \_ ChassisInRack**](cim-chassisinrack.md) rappresenta la relazione "contenitore" tra un rack e uno chassis in esso contenuto.

</dd> <dt>

[**Controllo \_ CIM**](cim-check.md)
</dt> <dd>

La [**classe CIM \_ Check**](cim-check.md) rappresenta una condizione o una caratteristica che deve essere vera in un ambiente definito o con ambito definito da un'istanza di [**una classe \_ ComputerSystem CIM.**](cim-computersystem.md) I controlli associati a un particolare elemento software sono organizzati in uno dei due gruppi usando la **proprietà Phase** dell'associazione [**CIM \_ SoftwareElementChecks.**](cim-softwareelementchecks.md)

</dd> <dt>

[**CIM \_ Chip**](cim-chip.md)
</dt> <dd>

La [**classe CIM \_ Chip**](cim-chip.md) rappresenta il tipo di hardware del circuito integrato, inclusi GLIC, processori, chip di memoria e così via.

</dd> <dt>

[**Clustering \_ CIMSAP**](cim-clusteringsap.md)
</dt> <dd>

La [**classe CIM \_ ClusteringSAP**](cim-clusteringsap.md) rappresenta i punti di accesso di un servizio di clustering.

</dd> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> <dd>

La [**classe CIM \_ ClusteringService**](cim-clusteringservice.md) rappresenta la funzionalità fornita da un cluster. Ad esempio, la funzionalità di failover può essere modellata come servizio di un cluster di failover.

</dd> <dt>

[**Cluster \_ CIMServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

La [**classe CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.

</dd> <dt>

[**Raccolte \_ CIM**](cim-collectedcollections.md)
</dt> <dd>

La [**classe CIM \_ CollectedCollections**](cim-collectedcollections.md) è un'associazione di aggregazione che rappresenta una raccolta di elementi di sistema gestiti (MSE) contenuti in una raccolta di MSE.

</dd> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> <dd>

La [**classe di associazione CIM \_ CollectedMSEs**](cim-collectedmses.md) rappresenta i membri dell'oggetto di raggruppamento, [**una classe CollectionOfMSEs.**](cim-collectionofmses.md)

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

[**L'oggetto CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) consente il raggruppamento di [**oggetti CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare impostazioni e configurazioni. È astratto richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.

</dd> <dt>

[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)
</dt> <dd>

[**L'associazione CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) rappresenta i sensori binari che costituiscono il sensore multistato.

</dd> <dt>

[**CIM \_ CollectionSetting**](cim-collectionsetting.md)
</dt> <dd>

La [**classe CIM \_ CollectionSetting**](cim-collectionsetting.md) rappresenta l'associazione tra [**un oggetto CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e la classe di impostazione definita per loro.

</dd> <dt>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)
</dt> <dd>

La classe [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) rappresenta un'associazione tra prodotti che indica se due prodotti a cui si fa riferimento sono interoperabili, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.

</dd> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> <dd>

[**L'associazione \_ del componente CIM**](cim-component.md) rappresenta le parti di una relazione tra mse.

</dd> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dd>

Una [**classe CIM \_ ComputerSystem**](cim-computersystem.md) rappresenta una raccolta speciale di [**istanze CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md) Questa raccolta fornisce le funzionalità del computer e funge da punto di aggregazione per associare uno o più degli elementi seguenti: file system, sistema operativo, processore e memoria (archiviazione volatile e non volatile). Questa classe è derivata da [**CIM \_ System**](cim-system.md).

</dd> <dt>

[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)
</dt> <dd>

La [**classe CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) rappresenta un'associazione tra un sistema di computer e i canali DMA (Direct Memory Access) disponibili.

</dd> <dt>

[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)
</dt> <dd>

La [**classe CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) rappresenta un'associazione tra un sistema informatico e le relative righe di richiesta di interrupt (IRQ) disponibili.

</dd> <dt>

[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)
</dt> <dd>

La [**classe CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) rappresenta un'associazione tra un sistema computer e le relative porte di I/O mappate alla memoria disponibili.

</dd> <dt>

[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)
</dt> <dd>

La [**classe CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) rappresenta un'associazione che definisce in modo esplicito la relazione tra sistemi computer unitari e uno o più pacchetti fisici. L'associazione è simile al modo in cui i dispositivi logici vengono realizzati da elementi fisici.

</dd> <dt>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> <dd>

La [**classe CIM \_ ComputerSystemResource**](cim-computersystemresource.md) rappresenta un'associazione tra un sistema computer e le relative risorse di sistema disponibili.

</dd> <dt>

[**Configurazione \_ CIM**](cim-configuration.md)
</dt> <dd>

[**L'oggetto \_ Configurazione CIM**](cim-configuration.md) consente il raggruppamento di set di parametri (definiti negli oggetti [**Impostazione \_ CIM)**](cim-setting.md) e dipendenze per uno o più elementi di sistema gestiti.

</dd> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> <dd>

La [**classe CIM \_ ConnectedTo**](cim-connectedto.md) rappresenta un'associazione che indica che due o più connettori fisici sono connessi.

</dd> <dt>

[**Connettore \_ CIMOnPackage**](cim-connectoronpackage.md)
</dt> <dd>

La [**classe CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) rappresenta un'associazione che rende esplicita la relazione di contenimento tra connettori e pacchetti. I pacchetti fisici contengono connettori e altri elementi fisici.

</dd> <dt>

[**Contenitore \_ CIM**](cim-container.md)
</dt> <dd>

La [**classe CIM \_ Container**](cim-container.md) rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore. Un oggetto contenitore deve essere un pacchetto fisico.

</dd> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dd>

La [**relazione CIM \_ ControlledBy**](cim-controlledby.md) indica i dispositivi a cui viene eseguito il comando o l'accesso tramite il dispositivo logico del controller.

</dd> <dt>

[**CIM \_ Controller**](cim-controller.md)
</dt> <dd>

La [**classe \_ controller CIM**](cim-controller.md) è una classe padre per il raggruppamento di dispositivi vari correlati al controllo. Esempi di controller sono controller SCSI, controller USB e controller seriali.

</dd> <dt>

[**CIM \_ CoolingDevice**](cim-coolingdevice.md)
</dt> <dd>

La [**classe CIM \_ CoolingDevice**](cim-coolingdevice.md) rappresenta le funzionalità e la gestione dei dispositivi di raffreddamento.

</dd> <dt>

[**CIM \_ CopyFileAction**](cim-copyfileaction.md)
</dt> <dd>

La [**classe CIM \_ CopyFileAction**](cim-copyfileaction.md) rappresenta lo spostamento o la copia di file da un sistema di computer a un nuovo percorso.

</dd> <dt>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)
</dt> <dd>

La [**classe CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crea directory vuote per l'installazione locale degli elementi software.

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

La [**classe CIM \_ CurrentSensor**](cim-currentsensor.md) esiste per garantire la compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dd>

La [**classe CIM \_ DataFile**](cim-datafile.md) rappresenta una raccolta denominata di dati o codice eseguibile. Verranno restituite solo le istanze di file nei dischi fissi locali

</dd> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dd>

La [**classe \_ Dependency CIM**](cim-dependency.md) rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.

</dd> <dt>

[**CIM \_ DependencyContext**](cim-dependencycontext.md)
</dt> <dd>

La [**relazione CIM \_ DependencyContext**](cim-dependencycontext.md) associa una [**classe \_ Dependency CIM**](cim-dependency.md) a uno o più [**oggetti di configurazione CIM. \_**](cim-configuration.md) Ad esempio, le dipendenze di un sistema informatico possono cambiare in base alla rete a cui è collegato il sistema.

</dd> <dt>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)
</dt> <dd>

La [**classe CIM \_ DesktopMonitor**](cim-desktopmonitor.md) rappresenta le funzionalità e la gestione del dispositivo logico CRT (Desktop Monitor).

</dd> <dt>

[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

La [**classe di associazione CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) specifica il dispositivo logico a cui si accede tramite la [**classe CIM \_ DeviceFile a**](cim-devicefile.md) cui si fa riferimento.

</dd> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> <dd>

La [**classe di associazione CIM \_ DeviceConnection**](cim-deviceconnection.md) rappresenta due o più dispositivi connessi.

</dd> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> <dd>

La [**classe CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico. I tipi di errori sono definiti da CCITT (Rec X.733) e ISO (IEC 10164-4).

</dd> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> <dd>

La [**classe CIM \_ DeviceFile**](cim-devicefile.md) rappresenta un tipo di file logico, che rappresenta un dispositivo. Questa convenzione è utile per i sistemi operativi che gestiscono i dispositivi usando un modello di I/O del flusso di byte. Il dispositivo logico associato a questo file viene specificato usando la [**relazione CIM \_ DeviceAccessedByFile.**](cim-deviceaccessedbyfile.md)

</dd> <dt>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dd>

La [**classe CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e la modalità di implementazione. Quando molti dispositivi logici sono associati a un sap, gli elementi operano in combinazione per fornire il punto di accesso. Se esistono implementazioni diverse di un sap, ogni implementazione comporta la creazione di singole istanze dell'oggetto SAP.

</dd> <dt>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)
</dt> <dd>

La [**classe CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) rappresenta un'associazione tra un servizio e la modalità di implementazione. Quando più dispositivi sono associati a un servizio, gli elementi operano insieme per fornire il servizio. Se esistono implementazioni diverse di un servizio, ogni implementazione comporta singole istanze dell'oggetto servizio.

</dd> <dt>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)
</dt> <dd>

La [**relazione CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica il software associato a un dispositivo, ad esempio driver, configurazione o software dell'applicazione o firmware.

</dd> <dt>

[**CIM \_ Directory**](cim-directory.md)
</dt> <dd>

La [**classe \_ Directory CIM**](cim-directory.md) rappresenta un tipo di file che raggruppa in modo logico i file di dati in essa contenuti e fornisce informazioni sul percorso per i file raggruppati.

</dd> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> <dd>

La [**classe astratta CIM \_ DirectoryAction**](cim-directoryaction.md) gestisce le directory. La creazione della directory viene gestita dalla [**classe \_ CIM CreateDirectoryAction**](cim-createdirectoryaction.md) e la rimozione della directory viene gestita dalla [**classe CIM \_ RemoveDirectoryAction.**](cim-removedirectoryaction.md)

</dd> <dt>

[**Directory \_ CIMContainsFile**](cim-directorycontainsfile.md)
</dt> <dd>

La [**classe CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) rappresenta un'associazione tra una directory e i file contenuti in tale directory.

</dd> <dt>

[**Directory \_ CIMSpecification**](cim-directoryspecification.md)
</dt> <dd>

La [**classe CIM \_ DirectorySpecification**](cim-directoryspecification.md) acquisisce la struttura di directory principale di un elemento software. Questa classe viene usata per organizzare i file di un elemento software in unità gestibili che possono essere rilocate in un sistema informatico.

</dd> <dt>

[**Directory \_ CIMSpecificationFile**](cim-directoryspecificationfile.md)
</dt> <dd>

[**L'associazione CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) rappresenta la directory che contiene il file specificato facendo riferimento alla [**classe CIM \_ DirectorySpecification.**](cim-directoryspecification.md)

</dd> <dt>

[**CIM \_ DiscreteSensor**](cim-discretesensor.md)
</dt> <dd>

La [**classe CIM \_ DiscreteSensor**](cim-discretesensor.md) include un set di valori stringa validi che può segnalare. I valori vengono enumerati nella proprietà **PossibleValues del** sensore. Un sensore discreto ha sempre una lettura corrente che corrisponde a uno dei valori enumerati.

</dd> <dt>

[**CIM \_ DiskDrive**](cim-diskdrive.md)
</dt> <dd>

La [**classe CIM \_ DiskDrive**](cim-diskdrive.md) rappresenta un'unità disco fisica, come illustrato dal sistema operativo. Le funzionalità dell'unità disco corrispondono alle caratteristiche logiche e di gestione dell'unità e, in alcuni casi, potrebbero non riflettere le caratteristiche fisiche del dispositivo. Un'interfaccia a un'unità fisica è un membro di questa classe. Tuttavia, un oggetto basato su un altro dispositivo logico non è un membro di questa classe.

</dd> <dt>

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)
</dt> <dd>

La [**classe CIM \_ DisketteDrive**](cim-diskettedrive.md) rappresenta le funzionalità e la gestione di un'unità dischetto.

</dd> <dt>

[**CIM \_ DiskPartition**](cim-diskpartition.md)
</dt> <dd>

La [**classe CIM \_ DiskPartition**](cim-diskpartition.md) rappresenta un intervallo contiguo di blocchi logici identificabili dal sistema operativo tramite i campi tipo e sottotipo della partizione. Le partizioni del disco devono essere realizzate direttamente da supporti fisici (indicati dall'associazione [**CIM \_ RealizesDiskPartition)**](cim-realizesdiskpartition.md) o create su volumi di archiviazione.

</dd> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> <dd>

La [**classe CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) controlla la quantità di spazio disponibile su disco del sistema e la specifica nella **proprietà AvailableDiskSpace.** I dettagli vengono confrontati con il valore nella proprietà **AvailableSpace** dell'oggetto [**\_ FileSystem CIM**](cim-filesystem.md) associato all'oggetto [**CIM \_ ComputerSystem,**](cim-computersystem.md) che descrive l'ambiente di sistema. Quando il valore della **proprietà AvailableSpace** è maggiore o uguale al valore specificato nella proprietà **AvailableDiskSpace,** la condizione viene soddisfatta.

</dd> <dt>

[**Visualizzazione \_ CIM**](cim-display.md)
</dt> <dd>

La [**classe CIM \_ Display**](cim-display.md) è una classe padre per il raggruppamento di dispositivi di visualizzazione vari.

</dd> <dt>

[**CIM \_ DMA**](cim-dma.md)
</dt> <dd>

La [**classe CIM \_ DMA**](cim-dma.md) rappresenta l'accesso diretto alla memoria (DMA) dell'architettura del computer.

</dd> <dt>

[**CIM \_ ancorato**](cim-docked.md)
</dt> <dd>

[**L'associazione \_ CIM Docked**](cim-docked.md) rappresenta la relazione tra due chassis. Ad esempio, un portatile (un tipo di chassis) può essere ancorato in un docking station (un altro tipo di chassis). Questa relazione tipica viene descritta in modo esplicito.

</dd> <dt>

[**Elemento \_ CIMCapacity**](cim-elementcapacity.md)
</dt> <dd>

La [**classe CIM \_ ElementCapacity**](cim-elementcapacity.md) associa un [**oggetto CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici. Associa una descrizione dei requisiti hardware minimi e massimi (o delle funzionalità) agli elementi fisici descritti.

</dd> <dt>

[**Elemento \_ CIMConfigurazione**](cim-elementconfiguration.md)
</dt> <dd>

[**L'associazione CIM \_ ElementConfiguration**](cim-elementconfiguration.md) mette in relazione un [**oggetto \_ Configurazione CIM**](cim-configuration.md) con uno o più elementi di sistema gestiti. **L'oggetto \_ Configurazione CIM** rappresenta un determinato comportamento o uno stato funzionale desiderato per [**l'oggetto CIM \_ ManagedSystemElement associato.**](cim-managedsystemelement.md)

</dd> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> <dd>

La [**classe CIM \_ ElementSetting**](cim-elementsetting.md) rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita per essi.

</dd> <dt>

[**Elementi \_ CIMLinked**](cim-elementslinked.md)
</dt> <dd>

[**L'associazione CIM \_ ElementsLinked**](cim-elementslinked.md) rappresenta gli elementi fisici collegati tra loro da un collegamento fisico.

</dd> <dt>

[**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md)
</dt> <dd>

La [**classe CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associa la [**classe CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) al dispositivo logico a cui si applica.

</dd> <dt>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)
</dt> <dd>

La [**classe CIM \_ ExecuteProgram**](cim-executeprogram.md) rappresenta i file che possono essere eseguiti nel sistema in cui è installato l'elemento software.

</dd> <dt>

[**Esportazione \_ CIM**](cim-export.md)
</dt> <dd>

La [**classe CIM \_ Export**](cim-export.md) rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio. Quando si esporta un intero file system, la directory deve fare riferimento alla directory più in alto del file system.

</dd> <dt>

[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)
</dt> <dd>

La [**classe CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) deriva da un gruppo di ridondanza che indica che gli elementi aggregati hanno più capacità o capacità di quanto sia necessario. Un esempio di questo tipo di ridondanza è l'installazione di alimentatori n+1 o ventole in un sistema.

</dd> <dt>

[**Ventola CIM \_**](cim-fan.md)
</dt> <dd>

La [**classe CIM \_ Fan**](cim-fan.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento a ventola.

</dd> <dt>

[**CIM \_ FileAction**](cim-fileaction.md)
</dt> <dd>

La [**classe CIM \_ FileAction**](cim-fileaction.md) consente all'autore di individuare i file già presenti nel computer di un utente e quindi di spostare o copiare tali file in un nuovo percorso.

</dd> <dt>

[**CIM \_ FileSpecification**](cim-filespecification.md)
</dt> <dd>

La [**classe CIM \_ FileSpecification**](cim-filespecification.md) rappresenta un file che si trova all'esterno o all'esterno del sistema. Il file si trova nella directory identificata [**dall'associazione CIM \_ DirectorySpecificationFile.**](cim-directoryspecificationfile.md) Il [**metodo Invoke**](invoke-method-in-class-cim-filespecification.md) usa le informazioni per verificare l'esistenza del file. Si noti che le proprietà con **un valore Null** non vengono controllate.

</dd> <dt>

[**CIM \_ FileStorage**](cim-filestorage.md)
</dt> <dd>

[**L'associazione CIM \_ FileStorage**](cim-filestorage.md) collega il file system e i file logici indirizzati tramite il file system.

</dd> <dt>

[**CIM \_ FileSystem**](cim-filesystem.md)
</dt> <dd>

La [**classe \_ FileSystem CIM**](cim-filesystem.md) rappresenta un file o un set di dati locale in un computer o montato in remoto da un file server.

</dd> <dt>

[**CIM \_ FlatPanel**](cim-flatpanel.md)
</dt> <dd>

La [**classe CIM \_ FlatPanel**](cim-flatpanel.md) rappresenta le funzionalità e la gestione del dispositivo logico del pannello flat.

</dd> <dt>

[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)
</dt> <dd>

[**L'associazione CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifica la directory di origine per l'azione file. Quando si usa questa associazione, si presuppone che la directory di origine sia stata creata da un'azione precedente. Questa associazione non può esistere con [**un'associazione CIM \_ FromDirectorySpecification.**](cim-fromdirectoryspecification.md) Un'azione di file può includere solo una singola directory di origine.

</dd> <dt>

[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)
</dt> <dd>

[**L'associazione CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifica la directory di origine per l'azione file. Quando si usa questa associazione, si presuppone che la directory di origine esista già. Questa associazione non può esistere con [**un'associazione CIM \_ FromDirectoryAction.**](cim-fromdirectoryaction.md) Un'azione file può coinvolgere solo una singola directory di origine.

</dd> <dt>

[**CIM \_ FRU**](cim-fru.md)
</dt> <dd>

La [**classe \_ FRU CIM**](cim-fru.md) rappresenta una raccolta definita dal fornitore di prodotti ed elementi fisici associati a un'unità sostituibile di campo (FRU) per supportare, gestire o aggiornare un prodotto nella sede del cliente.

</dd> <dt>

[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)
</dt> <dd>

La [**classe \_ CIM FRUIncludesProduct**](cim-fruincludesproduct.md) indica che un'unità sostituibile di campo può essere composta da altri prodotti.

</dd> <dt>

[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)
</dt> <dd>

La [**classe CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) rappresenta gli elementi fisici che costituiscono un'unità sostituibile di campo (FRU).

</dd> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> <dd>

La [**classe CIM \_ HeatPipe**](cim-heatpipe.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento a pipe termica.

</dd> <dt>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> <dd>

La [**classe CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornita. Ogni sistema può ospitare molti sap.

</dd> <dt>

[**CIM \_ HostedBootSAP**](cim-hostedbootsap.md)
</dt> <dd>

La [**classe CIM \_ HostedBootSAP**](cim-hostedbootsap.md) definisce il sistema di computer unitario di hosting per una [**classe CIM \_ BootSAP.**](cim-bootsap.md) Poiché questa relazione è sottoclassata da [**CIM \_ HostedAccessPoint,**](cim-hostedaccesspoint.md)eredita lo schema di ambito/denominazione definito per [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md), in cui un punto di accesso rinvia al sistema di hosting. In questo caso, **CIM \_ BootSAP** deve rinviare alla classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) di hosting.

</dd> <dt>

[**CIM \_ HostedBootService**](cim-hostedbootservice.md)
</dt> <dd>

La [**classe CIM \_ HostedBootService**](cim-hostedbootservice.md) associa un sistema di hosting e un servizio di avvio. Poiché questa relazione è sottoclassata da [**CIM \_ HostedService,**](cim-hostedservice.md)eredita lo schema di ambito/denominazione definito per il servizio, in cui un servizio rinvia al sistema di hosting.

</dd> <dt>

[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)
</dt> <dd>

[**L'associazione CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) rappresenta un collegamento tra il sistema computer e file system ospitata nel sistema computer.

</dd> <dt>

[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)
</dt> <dd>

La [**classe CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede. Un sistema può ospitare molte code di processi. Le destinazioni dei processi rimandano al sistema di hosting.

</dd> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dd>

La [**classe CIM \_ HostedService**](cim-hostedservice.md) rappresenta un'associazione tra un servizio e il sistema in cui si trova la funzionalità. Un sistema può ospitare molti servizi, che rimandano al sistema di hosting. Il modello non rappresenta i servizi ospitati in più sistemi.

</dd> <dt>

[**CIM \_ a raggi raggiro**](cim-infraredcontroller.md)
</dt> <dd>

La [**classe CIM \_ InfraredController**](cim-infraredcontroller.md) rappresenta le funzionalità e la gestione di un controller a raggi infrarossi.

</dd> <dt>

[**CIM \_ InstalledOS**](cim-installedos.md)
</dt> <dd>

La [**classe di associazione CIM \_ InstalledOS**](cim-installedos.md) rappresenta un collegamento tra il sistema computer e il sistema operativo installato. Un sistema operativo viene installato quando si trova nell'extent di archiviazione di un computer, ad esempio copiato in un'unità disco o scaricato in memoria.

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

La [**classe CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa un sistema computer a un elemento software installato.

</dd> <dt>

[**CIM \_ IRQ**](cim-irq.md)
</dt> <dd>

La [**classe CIM \_ IRQ**](cim-irq.md) rappresenta una riga di richiesta di interrupt dell'architettura Intel( IRQ).

</dd> <dt>

[**Processo \_ CIM**](cim-job.md)
</dt> <dd>

La [**classe CIM \_ Job**](cim-job.md) rappresenta un'unità di lavoro per un sistema, ad esempio un processo di stampa. Un processo è distinto da un processo perché un processo può essere pianificato.

</dd> <dt>

[**Processo \_ CIMDestination**](cim-jobdestination.md)
</dt> <dd>

La [**classe CIM \_ JobDestination**](cim-jobdestination.md) rappresenta la posizione in cui viene inviato un processo per l'elaborazione. Può fare riferimento a una coda che contiene zero o più processi, ad esempio una coda di stampa contenente processi di stampa. Le destinazioni dei processi sono ospitate nei sistemi, analogamente al modo in cui i servizi sono ospitati nei sistemi.

</dd> <dt>

[**Processi \_ CIMDestinationJobs**](cim-jobdestinationjobs.md)
</dt> <dd>

[**L'associazione CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) descrive dove viene inviato un processo per l'elaborazione, ovvero a quale destinazione del processo.

</dd> <dt>

[**Tastiera \_ CIM**](cim-keyboard.md)
</dt> <dd>

La [**classe CiM \_ Keyboard**](cim-keyboard.md) rappresenta le funzionalità e la gestione del dispositivo logico della tastiera.

</dd> <dt>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)
</dt> <dd>

La [**classe CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa i cavi e i collegamenti usati come connettori fisici, che connettono gli elementi fisici. Questa associazione definisce in modo esplicito la relazione dei connettori [**per CIM \_ PhysicalLink.**](cim-physicallink.md)

</dd> <dt>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)
</dt> <dd>

La [**classe CIM \_ LocalFileSystem**](cim-localfilesystem.md) rappresenta l'archivio file controllato da un sistema di computer tramite mezzi locali ,ad esempio l'accesso diretto al driver di dispositivo. L'archivio file può essere gestito direttamente dal sistema informatico, senza che un altro computer possa fungere da file server. Per un cluster file system, tuttavia, il file system è locale e, di conseguenza, rinvia al cluster.

</dd> <dt>

[**Percorso \_ CIM**](cim-location.md)
</dt> <dd>

La [**classe CIM \_ Location**](cim-location.md) rappresenta la posizione e l'indirizzo di un elemento fisico.

</dd> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dd>

La [**classe CIM \_ LogicalDevice**](cim-logicaldevice.md) rappresenta un'entità hardware che può essere realizzata o meno in hardware fisico.

</dd> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dd>

La [**classe CIM \_ LogicalDisk**](cim-logicaldisk.md) rappresenta un intervallo contiguo di blocchi logici identificabili da un file system tramite il campo **DeviceID** (chiave) del disco. Ad esempio, in un ambiente Windows, il **campo DeviceID** contiene una lettera di unità. in un UNIX, contiene il percorso di accesso. e in un ambiente NetWare contiene il nome del volume.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

La [**classe CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associa un disco logico alla partizione del disco in cui si trova.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

[**L'associazione CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) mette in relazione i dischi logici con il volume in cui vengono trovati. I dischi logici possono essere basati su un singolo volume (ad esempio esposto da un gestore di volumi software) o su una partizione del disco.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

La [**classe CIM \_ LogicalElement**](cim-logicalelement.md) è la classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

La [**classe CIM \_ LogicalFile**](cim-logicalfile.md) rappresenta una raccolta denominata di dati, che può essere codice eseguibile, che si trova in un file system in un extent di archiviazione.

</dd> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dd>

La [**classe CIM \_ LogicalIdentity**](cim-logicalidentity.md) è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.

</dd> <dt>

[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)
</dt> <dd>

La [**classe CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) rappresenta le funzionalità e la gestione di un'unità magneto-ottica, un sottotipo del dispositivo di accesso ai supporti.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

La [**classe CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) è la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.

</dd> <dt>

[**CIM \_ ManagementController**](cim-managementcontroller.md)
</dt> <dd>

La [**classe CIM \_ ManagementController**](cim-managementcontroller.md) è correlata alle funzionalità e alla gestione di un controller di gestione.

</dd> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> <dd>

La [**classe CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) rappresenta la possibilità di accedere a uno o più supporti e quindi di usare i supporti per archiviare e recuperare dati.

</dd> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dd>

[**L'associazione CIM \_ MediaPresent**](cim-mediapresent.md) descrive una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso ai supporti.

</dd> <dt>

[**Memoria \_ CIM**](cim-memory.md)
</dt> <dd>

La [**classe \_ CiM Memory**](cim-memory.md) rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.

</dd> <dt>

[**CIM \_ MemoryCapacity**](cim-memorycapacity.md)
</dt> <dd>

La [**classe CIM \_ MemoryCapacity**](cim-memorycapacity.md) rappresenta la memoria che può essere installata in un elemento fisico e le relative configurazioni minime e massime. Le informazioni sulla memoria attualmente installata e i requisiti minimi e massimi di un elemento si trovano nelle istanze della [**classe \_ CIM PhysicalMemory.**](cim-physicalmemory.md)

</dd> <dt>

[**CIM \_ MemoryCheck**](cim-memorycheck.md)
</dt> <dd>

La [**classe CIM \_ MemoryCheck**](cim-memorycheck.md) specifica una condizione per la quantità minima di memoria che deve essere disponibile in un sistema.

</dd> <dt>

[**Memoria \_ CIMMappedIO**](cim-memorymappedio.md)
</dt> <dd>

La [**classe CIM \_ MemoryMappedIO**](cim-memorymappedio.md) rappresenta l'I/O mappato alla memoria dell'architettura del computer. Questa classe risolve le risorse di I/O di memoria e porta.

</dd> <dt>

[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)
</dt> <dd>

La [**classe CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa la memoria fisica che si trova nelle schede di hosting, nelle schede adapter e così via. Questa associazione definisce in modo esplicito la relazione tra memoria e schede.

</dd> <dt>

[**Memoria \_ CIMConMedia**](cim-memorywithmedia.md)
</dt> <dd>

La [**classe CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.

</dd> <dt>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)
</dt> <dd>

La [**classe CIM \_ ModifySettingAction**](cim-modifysettingaction.md) rappresenta le informazioni per la modifica di un file di impostazione specifico, per una voce specifica, con un valore specifico.

</dd> <dt>

[**CIM \_ MonitorResolution**](cim-monitorresolution.md)
</dt> <dd>

La [**classe CIM \_ MonitorResolution**](cim-monitorresolution.md) rappresenta la relazione tra le risoluzioni orizzontale e verticale e la frequenza di aggiornamento e la modalità di analisi per un monitoraggio desktop. I valori vengono specificati nell'oggetto controller video.

</dd> <dt>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)
</dt> <dd>

La [**classe CIM \_ MonitorSetting**](cim-monitorsetting.md) associa la risoluzione del monitor al monitor desktop a cui si applica.

</dd> <dt>

[**Montaggio CIM \_**](cim-mount.md)
</dt> <dd>

La [**classe CIM \_ Mount**](cim-mount.md) rappresenta un'associazione tra un file system e una directory a cui è collegato.

</dd> <dt>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)
</dt> <dd>

La [**classe CIM \_ MultiStateSensor**](cim-multistatesensor.md) rappresenta un set multi-membro di sensori binari in cui ogni sensore binario segnala un risultato booleano.

</dd> <dt>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dd>

La [**classe CIM \_ NetworkAdapter**](cim-networkadapter.md) è una classe astratta che definisce i concetti generali relativi all'hardware di rete, ad esempio l'indirizzo permanente o la velocità di funzionamento. Le informazioni vengono trasmesse usando [**l'associazione CIM \_ DeviceSAPImplementation.**](cim-devicesapimplementation.md)

</dd> <dt>

[**CIM \_ NFS**](cim-nfs.md)
</dt> <dd>

La [**classe \_ NFS CIM**](cim-nfs.md) rappresenta un file system remoto montato, usando il protocollo NFS (Network file system), da un sistema informatico.

</dd> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

La [**classe CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) rappresenta le funzionalità e la gestione dell'archiviazione non volatile. La memoria non volatile include in modo nativo l'archiviazione flash e ROM.

</dd> <dt>

[**CIM \_ NumericSensor**](cim-numericsensor.md)
</dt> <dd>

La [**classe CIM \_ NumericSensor**](cim-numericsensor.md) rappresenta un sensore numerico che restituisce letture numeriche e supporta facoltativamente le impostazioni delle soglie.

</dd> <dt>

[**Sistema \_ operativo CIM**](cim-operatingsystem.md)
</dt> <dd>

La [**classe CIM \_ OperatingSystem**](cim-operatingsystem.md) rappresenta un sistema operativo del computer, costituito da software e firmware che rendono utilizzabile l'hardware di un sistema informatico.

</dd> <dt>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

La [**classe CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) rappresenta le funzionalità software che costituiscono il sistema operativo.

</dd> <dt>

[**CIM \_ OSProcess**](cim-osprocess.md)
</dt> <dd>

La [**classe CIM \_ OSProcess**](cim-osprocess.md) associa il sistema operativo e uno o più processi in esecuzione nel contesto del sistema operativo.

</dd> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> <dd>

La [**classe CIM \_ OSVersionCheck**](cim-osversioncheck.md) specifica le versioni del sistema operativo che possono supportare un elemento software.

</dd> <dt>

[**Pacchetto \_ CIMAlarm**](cim-packagealarm.md)
</dt> <dd>

[**L'associazione \_ CIM PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) rappresenta la relazione in cui un dispositivo di allarme viene installato come parte di un pacchetto. L'installazione indica problemi con l'ambiente del pacchetto, ovvero lo stato di sicurezza o l'integrità complessiva.

</dd> <dt>

[**CIM \_ PackageCooling**](cim-packagecooling.md)
</dt> <dd>

[**L'associazione CIM \_ PackageCooling**](cim-packagecooling.md) rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.

</dd> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dd>

[**L'associazione CIM \_ PackagedComponent**](cim-packagedcomponent.md) rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.

</dd> <dt>

[**CIM \_ PackageInChassis**](cim-packageinchassis.md)
</dt> <dd>

[**L'associazione \_ CiM PackageInChassis**](cim-packageinchassis.md) rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.

</dd> <dt>

[**Pacchetto \_ CIMInSlot**](cim-packageinslot.md)
</dt> <dd>

[**L'associazione \_ CIM PackageInSlot**](cim-packageinslot.md) rappresenta la relazione tra le schede dispositivo e lo chassis in cui sono montate.

</dd> <dt>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)
</dt> <dd>

[**L'associazione CIM \_ PackageTempSensor**](cim-packagetempsensor.md) rappresenta la relazione in cui un sensore temperatura viene spesso installato in un pacchetto, ad esempio uno chassis o un rack, per monitorare l'ambiente del pacchetto.

</dd> <dt>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)
</dt> <dd>

[**L'associazione CIM \_ ParallelController**](cim-parallelcontroller.md) è correlata alle funzionalità e alla gestione del dispositivo logico della porta parallela.

</dd> <dt>

[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)
</dt> <dd>

La [**classe CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica gli elementi fisici che devono essere sostituiti insieme.

</dd> <dt>

[**CIM \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

La [**classe \_ CIM PCIController**](cim-pcicontroller.md) rappresenta le proprietà e la gestione di un controller PCI. Le proprietà in questa classe e nelle relative sottoclassi sono definite nelle varie specifiche PCI pubblicate dal PCI SIG.

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

La [**classe \_ CIM PCMCIAController**](cim-pcmciacontroller.md) rappresenta le funzionalità e la gestione di un controller PCMCIA (Personal Computer Memory Card International Association).

</dd> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dd>

[**CIM \_ PCVideoController rappresenta**](cim-pcvideocontroller.md) le funzionalità e la gestione di un controller video personal computer, un sottotipo di controller video.

</dd> <dt>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

La [**classe CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) rappresenta gli extent fisici che fanno parte di un gruppo di ridondanza di archiviazione.

</dd> <dt>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)
</dt> <dd>

La [**classe \_ CiM PhysicalCapacity**](cim-physicalcapacity.md) è una classe astratta che rappresenta i requisiti minimi e massimi di un elemento fisico e la possibilità di supportare diversi tipi di hardware. Ad esempio, i requisiti di memoria minima e massima possono essere modellati come sottoclasse di **CIM \_ PhysicalCapacity**.

</dd> <dt>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dd>

La [**classe \_ CiM PhysicalComponent**](cim-physicalcomponent.md) rappresenta un componente di basso livello o di base all'interno di un pacchetto. Un elemento fisico che non è un collegamento, un connettore o un pacchetto è un discendente (o membro) di questa classe.

</dd> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> <dd>

La [**classe \_ CIM PhysicalConnector**](cim-physicalconnector.md) rappresenta qualsiasi elemento fisico usato per connettersi ad altri elementi. Qualsiasi oggetto in grado di connettersi e trasmettere segnali o potenza tra due o più elementi fisici è un discendente (o membro) di questa classe.

</dd> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> <dd>

Le [**\_ sottoclassi CIM PhysicalElement**](cim-physicalelement.md) definiscono qualsiasi componente di un sistema con un'identità fisica distinta. Le istanze di questa classe possono essere definite in termini di etichette che possono essere collegate fisicamente all'oggetto.

</dd> <dt>

[**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md)
</dt> <dd>

La [**classe CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associa un elemento fisico a un [**oggetto \_ Location CIM**](cim-location.md) a scopo di inventario o sostituzione.

</dd> <dt>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)
</dt> <dd>

La [**classe \_ CIM PhysicalExtent**](cim-physicalextent.md) rappresenta un'implementazione SCC RAID. Definisce gli indirizzi a blocchi indirizzabili consecutivi in un singolo dispositivo di archiviazione che vengono considerati come un singolo extent di archiviazione nella stessa [**classe CIM \_ StorageRedundancyGroup.**](cim-storageredundancygroup.md) In alternativa, quando si usa la configurazione automatica, è possibile creare un'istanza o estendere la [**classe \_ CIM AggregatePExtent.**](cim-aggregatepextent.md)

</dd> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> <dd>

La [**classe \_ CiM PhysicalFrame**](cim-physicalframe.md) è una classe padre di rack, chassis e altre enclosure di frame definite nelle classi di estensione. In questa classe padre sono incluse proprietà come **VisibleAlarm** e **AudibleAlarm** e i dati correlati alle violazioni della sicurezza.

</dd> <dt>

[**CIM \_ PhysicalLink**](cim-physicallink.md)
</dt> <dd>

La [**classe \_ CIM PhysicalLink**](cim-physicallink.md) rappresenta il cablaggio di elementi fisici.

</dd> <dt>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)
</dt> <dd>

La [**classe \_ CIM PhysicalMedia**](cim-physicalmedia.md) rappresenta i tipi di documentazione e supporto di archiviazione, ad esempio nastri, CD ROM e così via.

</dd> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

La [**classe \_ CIM PhysicalMemory**](cim-physicalmemory.md) rappresenta dispositivi di memoria di basso livello, ad esempio SIMMS, DIMM, chip di memoria non elaborata e così via.

</dd> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> <dd>

La [**classe \_ CiM PhysicalPackage**](cim-physicalpackage.md) rappresenta gli elementi fisici che contengono o ospitano altri componenti. Ad esempio, uno chassis rack o una scheda adattatore.

</dd> <dt>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dd>

La [**classe CIM \_ PointingDevice**](cim-pointingdevice.md) rappresenta un dispositivo che punta alle aree sullo schermo. Qualsiasi dispositivo che modifica un puntatore o punta ad aree in una visualizzazione visiva è un membro di questa classe. Ad esempio, mouse, stilo, touch pad o tablet.

</dd> <dt>

[**CIM \_ POTSModem**](cim-potsmodem.md)
</dt> <dd>

La [**classe CIM \_ POTSModem**](cim-potsmodem.md) rappresenta un dispositivo che converte i dati binari in modulazioni d'onda per la trasmissione basata sul suono connettendosi alla rete PLAIN Old Telephone System (POTS).

</dd> <dt>

[**CIM \_ PowerSupply**](cim-powersupply.md)
</dt> <dd>

La [**classe CIM \_ PowerSupply**](cim-powersupply.md) rappresenta le funzionalità e la gestione del dispositivo logico di alimentazione.

</dd> <dt>

[**Stampante \_ CIM**](cim-printer.md)
</dt> <dd>

La [**classe CIM \_ Printer**](cim-printer.md) rappresenta le funzionalità e la gestione del dispositivo logico della stampante.

</dd> <dt>

[**Processo \_ CIM**](cim-process.md)
</dt> <dd>

La [**classe Processo CIM \_**](cim-process.md) rappresenta una singola istanza di un programma in esecuzione. Un utente in genere vede un processo come un'applicazione o un'attività.

</dd> <dt>

[**CIM \_ ProcessExecutable**](cim-processexecutable.md)
</dt> <dd>

La [**classe CIM \_ ProcessExecutable**](cim-processexecutable.md) rappresenta un collegamento tra un processo e un file di dati e indica che il file partecipa all'esecuzione del processo.

</dd> <dt>

[**Processore CIM \_**](cim-processor.md)
</dt> <dd>

La [**classe \_ processore CIM**](cim-processor.md) rappresenta le funzionalità e la gestione del dispositivo logico del processore.

</dd> <dt>

[**Thread \_ processo CIM**](cim-processthread.md)
</dt> <dd>

La [**classe \_ CiM ProcessThread**](cim-processthread.md) rappresenta un collegamento tra un processo e i thread in esecuzione nel contesto del processo.

</dd> <dt>

[**Prodotto \_ CIM**](cim-product.md)
</dt> <dd>

La [**classe \_ Product CIM**](cim-product.md) è una classe concreta che rappresenta una raccolta di elementi fisici, funzionalità software e altri prodotti acquisiti come unità. L'acquisizione implica un accordo tra fornitore e consumer, che può avere implicazioni sulle licenze, sul supporto e sulla garanzia dei prodotti.

</dd> <dt>

[**CIM \_ ProductFRU**](cim-productfru.md)
</dt> <dd>

La [**classe CIM \_ ProductFRU**](cim-productfru.md) rappresenta un'associazione tra il prodotto e un'unità sostituibile (FRU) del campo, che fornisce informazioni sui componenti del prodotto che sono stati o sono stati sostituiti.

</dd> <dt>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)
</dt> <dd>

[**L'associazione CIM \_ ProductParentChild**](cim-productparentchild.md) definisce una gerarchia padre-figlio tra i prodotti. Ad esempio, un prodotto può essere in bundle con altri prodotti.

</dd> <dt>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)
</dt> <dd>

La [**classe CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) rappresenta gli elementi fisici che costituiscono un prodotto.

</dd> <dt>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)
</dt> <dd>

La [**classe CIM \_ ProductProductDependency**](cim-productproductdependency.md) rappresenta un'associazione tra due prodotti, che indica che uno deve essere installato o assente perché l'altro funzioni. Dal punto di vista concettuale è equivalente [**all'associazione \_ CiM ServiceServiceDependency.**](cim-serviceservicedependency.md)

</dd> <dt>

[**Prodotto \_ CIMSoftwareFeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

[**L'associazione CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica le funzionalità software per un determinato prodotto.

</dd> <dt>

[**CIM \_ ProductSupport**](cim-productsupport.md)
</dt> <dd>

La [**classe CIM \_ ProductSupport**](cim-productsupport.md) rappresenta un'associazione tra l'accesso al prodotto e al supporto tecnico che indica come viene ottenuto il supporto per il prodotto. Per un prodotto sono disponibili vari tipi di supporto. Lo stesso oggetto di supporto può fornire assistenza per più prodotti.

</dd> <dt>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)
</dt> <dd>

La [**classe CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) rappresenta gli indirizzi a blocchi logici indirizzabili, che vengono considerati come un singolo extent di archiviazione, ma si trovano in un singolo extent fisico.

</dd> <dt>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)
</dt> <dd>

La [**classe \_ CIM PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa gli extent dello spazio protetto basati su un extent fisico.

</dd> <dt>

[**CIM \_ Rack**](cim-rack.md)
</dt> <dd>

La [**classe CIM \_ Rack**](cim-rack.md) rappresenta un rack (un frame fisico o uno chassis) in cui sono archiviati gli chassis. In genere, un rack rappresenta l'enclosure. tutti i componenti funzionanti sono in pacchetto nello chassis.

</dd> <dt>

[**CIM \_ Realizes**](cim-realizes.md)
</dt> <dd>

La [**classe CIM \_ Realizes**](cim-realizes.md) rappresenta l'associazione che definisce il mapping tra un dispositivo logico e il componente fisico che implementa il dispositivo.

</dd> <dt>

[**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md)
</dt> <dd>

[**L'associazione CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) rappresenta la relazione in cui la [**classe CIM \_ AggregatePExtent**](cim-aggregatepextent.md) viene realizzata su un supporto fisico.

</dd> <dt>

[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)
</dt> <dd>

La [**classe CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) rappresenta una partizione del disco in un supporto fisico che modella la creazione di partizioni in un'unità SCSI o IDE non elaborata.

</dd> <dt>

[**CIM \_ RealizesPExtent**](cim-realizespextent.md)
</dt> <dd>

[**L'associazione CIM \_ RealizesPExtent**](cim-realizespextent.md) rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico. Viene inoltre specificato l'indirizzo iniziale dell'extent fisico nel supporto fisico.

</dd> <dt>

[**CIM \_ RebootAction**](cim-rebootaction.md)
</dt> <dd>

La [**classe CIM \_ RebootAction**](cim-rebootaction.md) causa un riavvio del sistema in cui è installato l'elemento software.

</dd> <dt>

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> <dd>

La [**classe CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associa un gruppo di ridondanza costituito da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono ridondanza. Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.

</dd> <dt>

[**Gruppo di \_ ridondanza CIM**](cim-redundancygroup.md)
</dt> <dd>

La [**classe CIM \_ RedundancyGroup**](cim-redundancygroup.md) rappresenta una raccolta di elementi di sistema gestiti, che indica che i componenti aggregati, insieme, forniscono ridondanza. Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.

</dd> <dt>

[**Refrigerazione CIM \_**](cim-refrigeration.md)
</dt> <dd>

La [**classe \_ REFRIGERATION CIM**](cim-refrigeration.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento refrigerante.

</dd> <dt>

[**CIM \_ RelatedStatistics**](cim-relatedstatistics.md)
</dt> <dd>

[**L'associazione CIM \_ RelatedStatistics**](cim-relatedstatistics.md) rappresenta gerarchie e dipendenze delle [**classi CIM \_ StatisticalInformation**](cim-statisticalinformation.md) correlate.

</dd> <dt>

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)
</dt> <dd>

La [**classe CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) rappresenta un file system remoto a cui si accede tramite un servizio correlato alla rete. In questo caso, l'archivio file è ospitato da un computer, che funge da file server.

</dd> <dt>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)
</dt> <dd>

La [**classe CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) rimuove le directory per gli elementi software.

</dd> <dt>

[**CIM \_ RemoveFileAction**](cim-removefileaction.md)
</dt> <dd>

La [**classe CIM \_ RemoveFileAction**](cim-removefileaction.md) disinstalla i file.

</dd> <dt>

[**CIM \_ ReplacementSet**](cim-replacementset.md)
</dt> <dd>

La [**classe CIM \_ ReplacementSet**](cim-replacementset.md) aggrega gli elementi fisici che devono essere sostituiti insieme. Ad esempio, quando si sostituisce una scheda di memoria, è possibile rimuovere e sostituire anche i chip di memoria dei componenti. In caso contrario, questa associazione può essere usata per sostituire o aggiornare un set di chip di memoria.

</dd> <dt>

[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)
</dt> <dd>

La [**classe CIM \_ ResidesOnExtent**](cim-residesonextent.md) rappresenta un'associazione tra un file system e l'extent di archiviazione in cui si trova. In genere, file system si trova in un disco logico.

</dd> <dt>

[**CIM \_ RunningOS**](cim-runningos.md)
</dt> <dd>

La [**classe CIM \_ RunningOS**](cim-runningos.md) rappresenta il sistema operativo attualmente in esecuzione. Al massimo, un sistema operativo può essere eseguito in qualsiasi momento in un sistema computer; il sistema potrebbe non essere attualmente avviato o il sistema operativo potrebbe essere sconosciuto.

</dd> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> <dd>

La [**classe CIM \_ SAPSAPDependency**](cim-sapsapdependency.md) è un'associazione tra due punti di accesso al servizio (SAP), che indica che il secondo SAP è necessario per la connessione del primo SAP al servizio.

</dd> <dt>

[**CIM \_ Scanner**](cim-scanner.md)
</dt> <dd>

Lo [**\_ scanner CIM**](cim-scanner.md) rappresenta le funzionalità e la gestione del dispositivo logico dello scanner.

</dd> <dt>

[**CIM \_ SCSIController**](cim-scsicontroller.md)
</dt> <dd>

La [**classe CIM \_ SCSIController**](cim-scsicontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico controller SCSI.

</dd> <dt>

[**CIM \_ SCSIInterface**](cim-scsiinterface.md)
</dt> <dd>

rappresenta una [**relazione CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite un controller SCSI e le caratteristiche di accesso.

</dd> <dt>

[**Sensore \_ CIM**](cim-sensor.md)
</dt> <dd>

La [**classe CiM \_ Sensor**](cim-sensor.md) rappresenta un dispositivo hardware in grado di misurare le caratteristiche di una proprietà fisica, ad esempio le caratteristiche di temperatura o tensione di un sistema informatico unitario.

</dd> <dt>

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> <dd>

La [**classe CIM \_ SerialController**](cim-serialcontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico della porta seriale.

</dd> <dt>

[**Interfaccia \_ seriale CIM**](cim-serialinterface.md)
</dt> <dd>

La [**classe CIM \_ SerialInterface**](cim-serialinterface.md) rappresenta una [**relazione CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.

</dd> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> <dd>

La [**classe \_ di servizio CIM**](cim-service.md) rappresenta un elemento logico che contiene informazioni per rappresentare e gestire le funzionalità fornite da un dispositivo o da una funzionalità software. Un servizio è un oggetto per utilizzo generico per configurare e gestire l'implementazione delle funzionalità. non è la funzionalità stessa.

</dd> <dt>

[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)
</dt> <dd>

La [**classe di associazione CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) rappresenta i punti di accesso per un servizio. Ad esempio, una stampante può essere accessibile da NetWare, Macintosh o Windows punti di accesso del servizio (SAP), potenzialmente ospitati in sistemi diversi.

</dd> <dt>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dd>

La [**classe CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) rappresenta la possibilità di usare o richiamare un servizio. I punti di accesso rappresentano i servizi disponibili per l'uso da parte di altre entità.

</dd> <dt>

[**Servizio \_ CIMSAPDependency**](cim-servicesapdependency.md)
</dt> <dd>

La [**classe CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP), che indica che sap a cui si fa riferimento viene usato dal servizio per fornire la relativa funzionalità.

</dd> <dt>

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)
</dt> <dd>

La [**classe CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) rappresenta un'associazione tra due servizi.

</dd> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dd>

La [**classe CIM \_ Setting**](cim-setting.md) rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.

</dd> <dt>

[**CIM \_ SettingCheck**](cim-settingcheck.md)
</dt> <dd>

La [**classe CIM \_ SettingCheck**](cim-settingcheck.md) specifica le informazioni necessarie per controllare un file di impostazione specifico per una voce specifica che contiene un valore uguale al valore specificato. Si presuppone che tutti i confronti non prescindono dalla distinzione tra maiuscole e minuscole.

</dd> <dt>

[**CIM \_ SettingContext**](cim-settingcontext.md)
</dt> <dd>

La [**classe CIM \_ SettingContext**](cim-settingcontext.md) associa gli oggetti di configurazione agli oggetti impostazione.

</dd> <dt>

[**CIM \_ Slot**](cim-slot.md)
</dt> <dd>

La [**classe \_ SLOT CIM**](cim-slot.md) rappresenta i connettori in cui vengono inseriti i pacchetti.

</dd> <dt>

[**Slot \_ CIMInSlot**](cim-slotinslot.md)
</dt> <dd>

La [**relazione CIM \_ SlotInSlot**](cim-slotinslot.md) rappresenta la possibilità di un adattatore speciale di estendere la struttura dello slot esistente per consentire il collegamento di schede altrimenti incompatibili a un frame o a una scheda di hosting.

</dd> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> <dd>

La [**classe CIM \_ SoftwareElement**](cim-softwareelement.md) scompone un oggetto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) in un set di parti gestibili singolarmente o distribuibili per una determinata piattaforma. La piattaforma di un elemento software è identificata in modo univoco dall'architettura hardware e dal sistema operativo sottostanti.

</dd> <dt>

[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)
</dt> <dd>

[**L'associazione CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifica le azioni per un elemento software.

</dd> <dt>

[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)
</dt> <dd>

La [**classe di associazione CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) mette in relazione un elemento software con informazioni sulla condizione o sulla posizione che una funzionalità può richiedere.

</dd> <dt>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)
</dt> <dd>

La [**classe CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) rappresenta un tipo di elemento software che deve esistere nell'ambiente.

</dd> <dt>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> <dd>

La [**classe CIM \_ SoftwareFeature**](cim-softwarefeature.md) rappresenta una funzione o una funzionalità specifica di un prodotto o di un sistema di applicazioni.

</dd> <dt>

[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

La [**classe CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e la modalità di implementazione nel software.

</dd> <dt>

[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

La [**classe CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) rappresenta un'associazione tra un servizio e la modalità di implementazione nel software.

</dd> <dt>

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

[**L'associazione CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica gli elementi software che costituiscono una funzionalità software specifica.

</dd> <dt>

[**CIM \_ SpareGroup**](cim-sparegroup.md)
</dt> <dd>

La [**classe CIM \_ SpareGroup**](cim-sparegroup.md) deriva dalla classe [**\_ CIM RedundancyGroup**](cim-redundancygroup.md) e indica che è possibile risparmiare uno o più elementi aggregati.

</dd> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dd>

La [**classe CIM \_ StatisticalInformation**](cim-statisticalinformation.md) è una classe radice per la raccolta arbitraria di dati statistici o metriche applicabili a uno o più elementi di sistema gestiti.

</dd> <dt>

[**Statistiche \_ CIM**](cim-statistics.md)
</dt> <dd>

La [**classe CIM \_ Statistics**](cim-statistics.md) rappresenta un'associazione che mette in relazione gli elementi di sistema gestiti con i gruppi statistici che si applicano a essi.

</dd> <dt>

[**CIM \_ StorageDefect**](cim-storagedefect.md)
</dt> <dd>

[**L'aggregazione CIM \_ StorageDefect**](cim-storagedefect.md) raccoglie gli errori di archiviazione per un extent di archiviazione.

</dd> <dt>

[**ERRORE DI ARCHIVIAZIONE CIM \_**](cim-storageerror.md)
</dt> <dd>

La [**classe CIM \_ StorageError**](cim-storageerror.md) rappresenta blocchi di supporti o di spazio di memoria di cui è stato eseguito il mapping non in uso a causa di errori. La chiave della classe è la **proprietà StartingAddress** dei byte in errore.

</dd> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> <dd>

La [**classe CIM \_ StorageExtent**](cim-storageextent.md) rappresenta le funzionalità e la gestione dei vari supporti esistenti per archiviare i dati e consentire il recupero dei dati. Questa classe padre può rappresentare i vari componenti di RAID (hardware o software) o un extent logico non elaborato su supporti fisici.

</dd> <dt>

[**Gruppo di \_ ridondanza dell'archiviazione CIM**](cim-storageredundancygroup.md)
</dt> <dd>

La [**classe CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) rappresenta le informazioni di ridondanza correlate all'archiviazione di massa.

</dd> <dt>

[**Supporto \_ CIMAccess**](cim-supportaccess.md)
</dt> <dd>

La [**classe \_ CiM SupportAccess**](cim-supportaccess.md) definisce come ottenere assistenza per un prodotto.

</dd> <dt>

[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)
</dt> <dd>

La [**classe CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) specifica la quantità di spazio di swapping che deve essere disponibile nel sistema.

</dd> <dt>

[**Sistema \_ CIM**](cim-system.md)
</dt> <dd>

La [**classe \_ System CIM**](cim-system.md) aggrega un set enumerabile di elementi di sistema gestiti. L'aggregazione funziona nel suo complesso funzionale. All'interno di una particolare sottoclasse del sistema è disponibile un elenco ben definito di classi di elementi di sistema gestite le cui istanze devono essere aggregate.

</dd> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

Classe Common Information Model di associazione cim (Common Information Model) che stabilisce relazioni tra un sistema e gli elementi di sistema gestiti di cui è composto.

</dd> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dd>

[**L'associazione \_ CiM SystemDevice**](cim-systemdevice.md) rappresenta una relazione esplicita in cui i dispositivi logici possono essere aggregati da un sistema.

</dd> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dd>

La [**classe \_ SystemResource CIM**](cim-systemresource.md) rappresenta un'entità gestita dal BIOS o un sistema operativo disponibile per l'uso da parte di software e dispositivi logici.

</dd> <dt>

[**CIM \_ Tachometer**](cim-tachometer.md)
</dt> <dd>

La [**classe CIM \_ Tachometer esiste**](cim-tachometer.md) per garantire la compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**CIM \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

La [**classe \_ CIM TapeDrive**](cim-tapedrive.md) rappresenta un'unità nastro nel sistema. Le unità nastro si distinguono principalmente per il fatto che è possibile accedervi solo in sequenza.

</dd> <dt>

[**CIM \_ TemperatureSensor**](cim-temperaturesensor.md)
</dt> <dd>

La [**classe CIM \_ TemperatureSensor esiste**](cim-temperaturesensor.md) per garantire la compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**CIM \_ Thread**](cim-thread.md)
</dt> <dd>

La [**classe \_ Thread CIM**](cim-thread.md) rappresenta la possibilità di eseguire unità di un processo o di un'attività, in parallelo. Un processo può avere molti thread, ognuno dei quali è debole per il processo.

</dd> <dt>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)
</dt> <dd>

[**L'associazione CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifica la directory di destinazione per l'azione file.

</dd> <dt>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)
</dt> <dd>

[**L'associazione CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica la directory di destinazione per l'azione file.

</dd> <dt>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

La [**classe CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) rappresenta le funzionalità e la gestione di un alimentatore (UPS) ininterrotto.

</dd> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dd>

La [**classe CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) rappresenta un computer desktop, mobile, di rete, un server o un altro tipo di computer a nodo singolo.

</dd> <dt>

[**CIM \_ USBController**](cim-usbcontroller.md)
</dt> <dd>

La [**classe CIM \_ USBController**](cim-usbcontroller.md) rappresenta le funzionalità e la gestione di un controller USB.

</dd> <dt>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)
</dt> <dd>

La [**classe CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) definisce gli hub downstream del controller USB.

</dd> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> <dd>

La [**classe CIM \_ USBDevice**](cim-usbdevice.md) rappresenta le caratteristiche di gestione di un dispositivo USB.

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

La [**classe \_ CIM USBHub**](cim-usbhub.md) rappresenta le funzionalità e la gestione di un hub USB.

</dd> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> <dd>

La [**classe \_ CIM UserDevice**](cim-userdevice.md) è una classe padre da cui discendono altre classi, ad esempio [**CIM \_ Keyboard**](cim-keyboard.md) o [**CIM \_ DesktopMonitor.**](cim-desktopmonitor.md) I dispositivi utente sono dispositivi logici che consentono all'utente di un computer di immettere, visualizzare o ascoltare i dati.

</dd> <dt>

[**VersionCompatibilityCheck di CIM \_**](cim-versioncompatibilitycheck.md)
</dt> <dd>

La [**classe CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) specifica se è consentito creare lo stato successivo di un elemento software.

</dd> <dt>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)
</dt> <dd>

La [**classe CIM \_ VideoBIOSElement**](cim-videobioselement.md) rappresenta il software di basso livello caricato nell'archiviazione non volatile e usato per configurare e accedere al controller video e alla visualizzazione di un computer.

</dd> <dt>

[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)
</dt> <dd>

La [**classe CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) rappresenta le funzionalità del software di basso livello usato per configurare e accedere al controller video e alla visualizzazione di un computer.

</dd> <dt>

[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

La [**classe CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa una funzionalità BIOS video e i relativi elementi BIOS video aggregati.

</dd> <dt>

[**CIM \_ VideoController**](cim-videocontroller.md)
</dt> <dd>

La [**classe CIM \_ VideoController**](cim-videocontroller.md) rappresenta le funzionalità e la gestione del controller video.

</dd> <dt>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)
</dt> <dd>

La [**classe CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) rappresenta le varie modalità video supportate da un controller video.

</dd> <dt>

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dd>

La [**classe CIM \_ VideoSetting**](cim-videosetting.md) associa l'oggetto impostazione [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) al controller a cui si applica.

</dd> <dt>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

La [**classe CIM \_ VolatileStorage**](cim-volatilestorage.md) rappresenta le funzionalità e la gestione dell'archiviazione volatile.

</dd> <dt>

[**CIM \_ VoltageSensor**](cim-voltagesensor.md)
</dt> <dd>

La [**classe CIM \_ VoltageSensor esiste**](cim-voltagesensor.md) per garantire la compatibilità con le versioni precedenti delle definizioni dello schema CIM. Con le aggiunte [**alle classi CiM \_ Sensor**](cim-sensor.md) e [**CIM \_ NumericSensor**](cim-numericsensor.md) nella versione 2.2, non è più necessario.

</dd> <dt>

[**CIM \_ VolumeSet**](cim-volumeset.md)
</dt> <dd>

La [**classe \_ VolumeSet CIM**](cim-volumeset.md) rappresenta un intervallo contiguo di blocchi logici presentati all'ambiente operativo per la lettura e la scrittura dei dati utente.

</dd> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> <dd>

La [**classe CIM \_ WORMDrive**](cim-wormdrive.md) rappresenta le funzionalità e la gestione di un'unità WORM, un sottotipo del dispositivo di accesso ai supporti.

</dd> </dl>

 

 
