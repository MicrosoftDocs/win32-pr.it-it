---
description: Queste classi WMI sono dichiarate in CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Provider WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523106"
---
# <a name="cim-wmi-provider"></a>Provider WMI CIM

Queste classi WMI sono dichiarate in CimWin32. mof.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**\_Azione CIM**](cim-action.md)
</dt> <dd>

Una classe di [**\_ azione CIM**](cim-action.md) è un'operazione che fa parte di un processo per creare un elemento software nello stato successivo o per eliminare l'elemento software nello stato corrente.

</dd> <dt>

[**\_ACTIONSEQUENCE CIM**](cim-actionsequence.md)
</dt> <dd>

L'associazione [**CIM \_ ActionSequence**](cim-actionsequence.md) definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.

</dd> <dt>

[**\_ACTSASSPARE CIM**](cim-actsasspare.md)
</dt> <dd>

L'associazione [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indica gli elementi che possono essere sostituiti o sostituiti da altri elementi aggregati. Una scorta può funzionare in modalità "hot-standby", come specificato in base a un elemento.

</dd> <dt>

[**\_ADJACENTSLOTS CIM**](cim-adjacentslots.md)
</dt> <dd>

L'associazione [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) descrive il layout degli slot in una scheda di hosting o scheda di scheda. Le informazioni, ad esempio la distanza tra gli slot e il fatto che siano "condivise" (se ne viene popolato uno, non è possibile usare l'altro slot), vengono trasmesse come proprietà di associazione.

</dd> <dt>

[**\_AGGREGATEPEXTENT CIM**](cim-aggregatepextent.md)
</dt> <dd>

La classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fornisce informazioni di riepilogo sui blocchi logici indirizzabili, che si trovano nello stesso gruppo di ridondanza di archiviazione e si trovano nello stesso supporto fisico.

</dd> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> <dd>

La classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) definisce il numero di blocchi logici indirizzabili in un singolo dispositivo di archiviazione, esclusi i blocchi logici mappati come dati di controllo. Se vengono definiti set di volumi, i blocchi logici sono contenuti all'interno di un singolo set di volumi. Si tratta di un raggruppamento alternativo per [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), quando sono necessarie solo le informazioni di riepilogo o quando si usa la configurazione automatica.

</dd> <dt>

[**\_AGGREGATEREDUNDANCYCOMPONENT CIM**](cim-aggregateredundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.

</dd> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> <dd>

La classe [**CIM \_ AlarmDevice**](cim-alarmdevice.md) è un dispositivo di allarme che emette indicazioni udibili o visibili correlate alla situazione di un problema.

</dd> <dt>

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dd>

La classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.

</dd> <dt>

[**\_APPLICATIONSYSTEM CIM**](cim-applicationsystem.md)
</dt> <dd>

La classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) rappresenta un'applicazione o un sistema software che supporta una particolare funzione di business che può essere gestita come unità indipendente. Un sistema di questo tipo può essere scomposto nei componenti funzionali usando la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) . Le funzionalità software per una particolare applicazione o sistema software si trovano usando l'associazione [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .

</dd> <dt>

[**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

La classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo. Le funzionalità software possono essere incluse in prodotti diversi.

</dd> <dt>

[**\_ASSOCIATEDALARM CIM**](cim-associatedalarm.md)
</dt> <dd>

La dipendenza [**CIM \_ AssociatedAlarm**](cim-associatedalarm.md) associa un allarme a un dispositivo logico.

</dd> <dt>

[**\_ASSOCIATEDBATTERY CIM**](cim-associatedbattery.md)
</dt> <dd>

La dipendenza [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) associa una batteria a un dispositivo logico. Usare questa associazione per modellare singole batterie che costituiscono un gruppo di continuità (UPS, Power Supply).

</dd> <dt>

[**\_ASSOCIATEDCOOLING CIM**](cim-associatedcooling.md)
</dt> <dd>

L'associazione [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indica quando le ventole o altri dispositivi di raffreddamento sono specifici di un dispositivo (rispetto alla custodia o al raffreddamento del cabinet).

</dd> <dt>

[**\_ASSOCIATEDMEMORY CIM**](cim-associatedmemory.md)
</dt> <dd>

La classe [**CIM \_ AssociateMemory**](cim-associatedmemory.md) associa la memoria installata o associata, ad esempio la memoria della cache con un dispositivo logico.

</dd> <dt>

[**\_ASSOCIATEDPROCESSORMEMORY CIM**](cim-associatedprocessormemory.md)
</dt> <dd>

La classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associa il processore e la memoria di sistema o la cache di un processore.

</dd> <dt>

[**\_ASSOCIATEDSENSOR CIM**](cim-associatedsensor.md)
</dt> <dd>

La classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associa un sensore installato a un dispositivo logico. Il sensore misura le proprietà di input e output critiche e può essere incluso nel dispositivo o installato nelle vicinanze.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

La classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associa un alimentatore a un sensore corrente (amperaggio) che monitora la frequenza di input.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Associa un alimentatore a un sensore di tensione che monitora la tensione di input.

</dd> <dt>

[**\_BASEDON CIM**](cim-basedon.md)
</dt> <dd>

La classe [**CIM \_ BasedOn**](cim-basedon.md) rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore. Ad esempio, gli extent fisici includono extent dello spazio protetto. I set di volumi vengono quindi assemblati da uno o più extent di spazio fisico o protetto. La memoria cache può essere definita in modo indipendente e realizzata in un elemento fisico oppure può essere basata su extent di archiviazione volatili o non volatili.

</dd> <dt>

[**\_Batteria CIM**](cim-battery.md)
</dt> <dd>

La classe [**CIM \_ batteria**](cim-battery.md) rappresenta le funzionalità e la gestione del dispositivo logico della batteria. Questa classe si applica alle batterie nei sistemi portatili e altre batterie interne ed esterne.

</dd> <dt>

[**\_BINARYSENSOR CIM**](cim-binarysensor.md)
</dt> <dd>

La classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fornisce un output booleano. Sono state aggiunte le proprietà **CurrentState** e **PossibleStates** per i sensori, rendendo la sottoclasse **CIM \_ BinarySensor** non più necessaria, sebbene venga mantenuta per compatibilità con le versioni precedenti. È possibile creare un sensore binario creando un'istanza di un sensore con due stati possibili.

</dd> <dt>

[**CIM \_ bioselement**](cim-bioselement.md)
</dt> <dd>

La classe [**CIM \_ bioselement**](cim-bioselement.md) rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per avviare e configurare un sistema di computer.

</dd> <dt>

[**\_BIOSFEATURE CIM**](cim-biosfeature.md)
</dt> <dd>

rappresenta le funzionalità del software di basso livello utilizzato per avviare e configurare un sistema di computer.

</dd> <dt>

[**\_BIOSFEATUREBIOSELEMENTS CIM**](cim-biosfeaturebioselements.md)
</dt> <dd>

La classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associa una funzionalità BIOS e i relativi elementi BIOS aggregati.

</dd> <dt>

[**\_BIOSLOADEDINNV CIM**](cim-biosloadedinnv.md)
</dt> <dd>

La classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associa un elemento BIOS e l'archiviazione non volatile in cui viene caricata.

</dd> <dt>

[**\_BOOTOSFROMFS CIM**](cim-bootosfromfs.md)
</dt> <dd>

La classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associa il sistema operativo e i file System da cui viene caricato il sistema operativo. L'associazione è molti-a-molti; un sistema operativo distribuito può dipendere da diversi file System da caricare correttamente e completamente.

</dd> <dt>

[**\_BOOTSAP CIM**](cim-bootsap.md)
</dt> <dd>

La classe [**CIM \_ BootSAP**](cim-bootsap.md) rappresenta i punti di accesso di un servizio di avvio.

</dd> <dt>

[**\_BOOTSERVICE CIM**](cim-bootservice.md)
</dt> <dd>

La classe [**CIM \_ BOOTSERVICE**](cim-bootservice.md) rappresenta la funzionalità fornita da un dispositivo o un software, o da una rete, per caricare un sistema operativo in un computer di sistema.

</dd> <dt>

[**\_BOOTSERVICEACCESSBYSAP CIM**](cim-bootserviceaccessbysap.md)
</dt> <dd>

La classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associa un servizio di avvio e i relativi punti di accesso.

</dd> <dt>

[**\_CACHEMEMORY CIM**](cim-cachememory.md)
</dt> <dd>

La classe [**CIM \_ CacheMemory**](cim-cachememory.md) definisce le funzionalità e la gestione della memoria cache.

</dd> <dt>

[**\_Scheda CIM**](cim-card.md)
</dt> <dd>

La [**classe \_ CIM**](cim-card.md) rappresenta un tipo di contenitore fisico che può essere inserito in un'altra scheda o lavagna host oppure è una lavagna di hosting/scheda madre in uno chassis. Questa classe include tutti i pacchetti in grado di trasportare segnali e fornire un punto di montaggio per i componenti fisici, ad esempio chip o altri pacchetti fisici, ad esempio altre schede.

</dd> <dt>

[**\_CARDINSLOT CIM**](cim-cardinslot.md)
</dt> <dd>

La classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associa una scheda di adapter al contenitore in cui viene inserita.

</dd> <dt>

[**\_CARDONCARD CIM**](cim-cardoncard.md)
</dt> <dd>

L'associazione [**CIM \_ CardOnCard**](cim-cardoncard.md) descrive le relazioni sulle schede che possono essere inserite in schede madri/battiscopa, daughtercards di un adapter o schede che supportano moduli speciali di tipo scheda.

</dd> <dt>

[**\_CDROMDRIVE CIM**](cim-cdromdrive.md)
</dt> <dd>

La classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) rappresenta un'unità CD-ROM nel computer.

</dd> <dt>

[**\_Chassis CIM**](cim-chassis.md)
</dt> <dd>

La [**classe \_ chassis CIM**](cim-chassis.md) rappresenta gli elementi fisici che racchiudono altri elementi e fornisce funzionalità definibili, ad esempio un desktop, un nodo di elaborazione, un UPS, un'archiviazione su disco o su nastro o una combinazione di questi.

</dd> <dt>

[**\_CHASSISINRACK CIM**](cim-chassisinrack.md)
</dt> <dd>

L'associazione [**CIM \_ ChassisInRack**](cim-chassisinrack.md) rappresenta la relazione "containing" tra un rack e uno chassis che contiene.

</dd> <dt>

[**\_Controllo CIM**](cim-check.md)
</dt> <dd>

La classe [**CIM \_ Check**](cim-check.md) rappresenta una condizione o una caratteristica che dovrebbe essere true in un ambiente definito o con ambito da un'istanza di una classe [**CIM \_ ComputerSystem**](cim-computersystem.md) . I controlli associati a un particolare elemento software sono organizzati in uno dei due gruppi usando la proprietà **Phase** dell'associazione [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) .

</dd> <dt>

[**\_Chip CIM**](cim-chip.md)
</dt> <dd>

La classe [**CIM \_ chip**](cim-chip.md) rappresenta il tipo di hardware del circuito integrato, tra cui ASICS, processori, chip di memoria e così via.

</dd> <dt>

[**\_CLUSTERINGSAP CIM**](cim-clusteringsap.md)
</dt> <dd>

La classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) rappresenta i punti di accesso di un servizio di clustering.

</dd> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> <dd>

La classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) rappresenta la funzionalità fornita da un cluster. Ad esempio, la funzionalità di failover può essere modellata come servizio di un cluster di failover.

</dd> <dt>

[**\_CLUSTERSERVICEACCESSBYSAP CIM**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

La classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.

</dd> <dt>

[**\_COLLECTEDCOLLECTIONS CIM**](cim-collectedcollections.md)
</dt> <dd>

La classe [**CIM \_ CollectedCollections**](cim-collectedcollections.md) è un'associazione di aggregazione che rappresenta una raccolta di elementi di sistema gestiti (MSE) contenuti in una raccolta di mses.

</dd> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> <dd>

La classe di associazione [**CIM \_ CollectedMSEs**](cim-collectedmses.md) rappresenta i membri dell'oggetto GROUPING, una classe [**CollectionOfMSEs**](cim-collectionofmses.md) .

</dd> <dt>

[**\_COLLECTIONOFMSES CIM**](cim-collectionofmses.md)
</dt> <dd>

L'oggetto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) consente il raggruppamento di oggetti [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare le impostazioni e le configurazioni. È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.

</dd> <dt>

[**\_COLLECTIONOFSENSORS CIM**](cim-collectionofsensors.md)
</dt> <dd>

L'associazione [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) rappresenta i sensori binari che compongono il sensore multistato.

</dd> <dt>

[**\_COLLECTIONSETTING CIM**](cim-collectionsetting.md)
</dt> <dd>

La classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) rappresenta l'associazione tra un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) e la classe di impostazione definita.

</dd> <dt>

[**\_COMPATIBLEPRODUCT CIM**](cim-compatibleproduct.md)
</dt> <dd>

La classe [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.

</dd> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dd>

L' [**associazione \_ componente CIM**](cim-component.md) rappresenta le parti di una relazione tra mses.

</dd> <dt>

[**\_ComputerSystem CIM**](cim-computersystem.md)
</dt> <dd>

Una classe [**CIM \_ ComputerSystem**](cim-computersystem.md) rappresenta una raccolta speciale di istanze [**CIM di \_ ManagedSystemElement**](cim-managedsystemelement.md) . Questa raccolta fornisce funzionalità del computer e funge da punto di aggregazione per associare uno o più degli elementi seguenti: file system, sistema operativo, processore e memoria (archiviazione volatile e non volatile). Questa classe è derivata dal [**\_ sistema CIM**](cim-system.md).

</dd> <dt>

[**\_COMPUTERSYSTEMDMA CIM**](cim-computersystemdma.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.

</dd> <dt>

[**\_COMPUTERSYSTEMIRQ CIM**](cim-computersystemirq.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) rappresenta un'associazione tra un sistema di computer e le relative righe di richiesta di interrupt (IRQ) disponibili.

</dd> <dt>

[**\_COMPUTERSYSTEMMAPPEDIO CIM**](cim-computersystemmappedio.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.

</dd> <dt>

[**\_COMPUTERSYSTEMPACKAGE CIM**](cim-computersystempackage.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) rappresenta un'associazione che definisce in modo esplicito la relazione tra i sistemi di computer unitari e uno o più pacchetti fisici. L'associazione è simile al modo in cui i dispositivi logici vengono realizzati da elementi fisici.

</dd> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) rappresenta un'associazione tra un sistema di computer e le risorse di sistema disponibili.

</dd> <dt>

[**\_Configurazione CIM**](cim-configuration.md)
</dt> <dd>

L'oggetto di [**\_ configurazione CIM**](cim-configuration.md) consente il raggruppamento di set di parametri (definiti in oggetti [**\_ impostazione CIM**](cim-setting.md) ) e le dipendenze per uno o più elementi di sistema gestiti.

</dd> <dt>

[**\_CONNECTEDTO CIM**](cim-connectedto.md)
</dt> <dd>

La classe [**CIM \_ ConnectedTo**](cim-connectedto.md) rappresenta un'associazione che indica che due o più connettori fisici sono connessi.

</dd> <dt>

[**\_CONNECTORONPACKAGE CIM**](cim-connectoronpackage.md)
</dt> <dd>

La classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) rappresenta un'associazione che rende esplicita la relazione di contenimento tra i connettori e i pacchetti. I pacchetti fisici contengono connettori, oltre ad altri elementi fisici.

</dd> <dt>

[**\_Contenitore CIM**](cim-container.md)
</dt> <dd>

La [**classe \_ contenitore CIM**](cim-container.md) rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore. Un oggetto contenitore deve essere un pacchetto fisico.

</dd> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dd>

La relazione [**CIM \_ ControlledBy**](cim-controlledby.md) indica i dispositivi a cui viene eseguito il comando o a cui si accede tramite il dispositivo logico del controller.

</dd> <dt>

[**\_Controller CIM**](cim-controller.md)
</dt> <dd>

La classe del [**\_ controller CIM**](cim-controller.md) è una classe padre per il raggruppamento di dispositivi correlati al controllo. Esempi di controller sono controller SCSI, controller USB e controller seriali.

</dd> <dt>

[**\_COOLINGDEVICE CIM**](cim-coolingdevice.md)
</dt> <dd>

La classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) rappresenta le funzionalità e la gestione dei dispositivi di raffreddamento.

</dd> <dt>

[**\_COPYFILEACTION CIM**](cim-copyfileaction.md)
</dt> <dd>

La classe [**CIM \_ CopyFileAction**](cim-copyfileaction.md) rappresenta lo spostamento o la copia di file da un sistema di computer in una nuova posizione.

</dd> <dt>

[**\_CREATEDIRECTORYACTION CIM**](cim-createdirectoryaction.md)
</dt> <dd>

La classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crea directory vuote per gli elementi software da installare localmente.

</dd> <dt>

[**\_CURRENTSENSOR CIM**](cim-currentsensor.md)
</dt> <dd>

La classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dd>

La classe [**CIM \_ DataFile**](cim-datafile.md) rappresenta una raccolta denominata di dati o codice eseguibile. Verranno restituite solo le istanze di file nei dischi fissi locali

</dd> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> <dd>

La classe di [**\_ dipendenza CIM**](cim-dependency.md) rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.

</dd> <dt>

[**\_DEPENDENCYCONTEXT CIM**](cim-dependencycontext.md)
</dt> <dd>

La relazione [**CIM \_ DependencyContext**](cim-dependencycontext.md) associa una classe di [**\_ dipendenza CIM**](cim-dependency.md) a uno o più oggetti di [**\_ configurazione CIM**](cim-configuration.md) . Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.

</dd> <dt>

[**\_DESKTOPMONITOR CIM**](cim-desktopmonitor.md)
</dt> <dd>

La classe [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) rappresenta le funzionalità e la gestione del dispositivo logico monitor desktop (CRT).

</dd> <dt>

[**\_DEVICEACCESSEDBYFILE CIM**](cim-deviceaccessedbyfile.md)
</dt> <dd>

La classe di associazione [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) specifica il dispositivo logico a cui si accede tramite la classe [**CIM \_ DeviceFile**](cim-devicefile.md) a cui si fa riferimento.

</dd> <dt>

[**\_DEVICECONNECTION CIM**](cim-deviceconnection.md)
</dt> <dd>

La classe di associazione [**CIM \_ DeviceConnection**](cim-deviceconnection.md) rappresenta due o più dispositivi connessi.

</dd> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> <dd>

La classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico. I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).

</dd> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> <dd>

La classe [**CIM \_ DeviceFile**](cim-devicefile.md) rappresenta un tipo di file logico, che rappresenta un dispositivo. Questa convenzione è utile per i sistemi operativi che gestiscono I dispositivi usando un modello di I/O del flusso di byte. Il dispositivo logico associato a questo file viene specificato utilizzando la relazione [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .

</dd> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dd>

La classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato. Quando molti dispositivi logici sono associati a un SAP, gli elementi operano insieme per fornire il punto di accesso. Se esistono implementazioni diverse di un SAP, ogni implementazione genera singole creazioni di istanze dell'oggetto SAP.

</dd> <dt>

[**\_DEVICESERVICEIMPLEMENTATION CIM**](cim-deviceserviceimplementation.md)
</dt> <dd>

La classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) rappresenta un'associazione tra un servizio e il modo in cui viene implementata. Quando più dispositivi sono associati a un servizio, gli elementi operano insieme per fornire il servizio. Se esistono implementazioni diverse di un servizio, ogni implementazione produce singole creazioni di istanze dell'oggetto servizio.

</dd> <dt>

[**\_DEVICESOFTWARE CIM**](cim-devicesoftware.md)
</dt> <dd>

La relazione [**CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica il software associato a un dispositivo, ad esempio i driver, la configurazione o il software dell'applicazione o il firmware.

</dd> <dt>

[**\_Directory CIM**](cim-directory.md)
</dt> <dd>

La classe [**CIM \_ directory**](cim-directory.md) rappresenta un tipo di file che raggruppa logicamente i file di dati che contiene e fornisce informazioni sul percorso per i file raggruppati.

</dd> <dt>

[**\_DIRECTORYACTION CIM**](cim-directoryaction.md)
</dt> <dd>

La classe [**CIM \_ DirectoryAction**](cim-directoryaction.md) Abstract gestisce le directory. La creazione della directory viene gestita dalla classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) e la rimozione della directory viene gestita dalla classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .

</dd> <dt>

[**\_DIRECTORYCONTAINSFILE CIM**](cim-directorycontainsfile.md)
</dt> <dd>

La classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) rappresenta un'associazione tra una directory e i file contenuti all'interno di tale directory.

</dd> <dt>

[**\_DIRECTORYSPECIFICATION CIM**](cim-directoryspecification.md)
</dt> <dd>

La classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) acquisisce la struttura di directory principale di un elemento software. Questa classe viene utilizzata per organizzare i file di un elemento software in unità gestibili che possono essere rilocate in un sistema di computer.

</dd> <dt>

[**\_DIRECTORYSPECIFICATIONFILE CIM**](cim-directoryspecificationfile.md)
</dt> <dd>

L'associazione [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) rappresenta la directory che contiene il file specificato facendo riferimento alla classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .

</dd> <dt>

[**\_DISCRETESENSOR CIM**](cim-discretesensor.md)
</dt> <dd>

La classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) presenta un set di valori stringa validi che possono essere segnalati. I valori vengono enumerati nella proprietà **PossibleValues** del sensore. Un sensore discreto ha sempre una lettura corrente corrispondente a uno dei valori enumerati.

</dd> <dt>

[**\_DiskDrive CIM**](cim-diskdrive.md)
</dt> <dd>

La classe [**CIM \_ DiskDrive**](cim-diskdrive.md) rappresenta un'unità disco fisica visualizzata dal sistema operativo. Le funzionalità dell'unità disco corrispondono alle caratteristiche logiche e di gestione dell'unità e, in alcuni casi, potrebbero non riflettere le caratteristiche fisiche del dispositivo. Un'interfaccia a un'unità fisica è un membro di questa classe. Tuttavia, un oggetto basato su un altro dispositivo logico non è un membro di questa classe.

</dd> <dt>

[**\_DISKETTEDRIVE CIM**](cim-diskettedrive.md)
</dt> <dd>

La classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) rappresenta le funzionalità e la gestione di un'unità floppy.

</dd> <dt>

[**\_DISKPARTITION CIM**](cim-diskpartition.md)
</dt> <dd>

La classe [**CIM \_ DiskPartition**](cim-diskpartition.md) rappresenta un intervallo contiguo di blocchi logici identificabili dal sistema operativo mediante i campi tipo e sottotipo della partizione. Le partizioni disco devono essere realizzate direttamente da supporti fisici (indicati dall'associazione [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) ) o basate su volumi di archiviazione.

</dd> <dt>

[**\_DISKSPACECHECK CIM**](cim-diskspacecheck.md)
</dt> <dd>

La classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) controlla la quantità di spazio disponibile su disco del sistema e la specifica nella proprietà **AvailableDiskSpace** . I dettagli vengono confrontati con il valore nella proprietà **AvailableSpace** dell'oggetto [**\_ file System CIM**](cim-filesystem.md) associato all'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) , che descrive l'ambiente di sistema. Se il valore della proprietà **AvailableSpace** è maggiore o uguale al valore specificato nella proprietà **AvailableDiskSpace** , la condizione viene soddisfatta.

</dd> <dt>

[**\_Visualizzazione CIM**](cim-display.md)
</dt> <dd>

La classe di [**\_ visualizzazione CIM**](cim-display.md) è una classe padre per il raggruppamento di periferiche di visualizzazione varie.

</dd> <dt>

[**\_DMA CIM**](cim-dma.md)
</dt> <dd>

La classe [**CIM \_ DMA**](cim-dma.md) rappresenta l'accesso diretto alla memoria (DMA) dell'architettura del computer.

</dd> <dt>

[**CIM \_ ancorato**](cim-docked.md)
</dt> <dd>

L'associazione di [**CIM \_ ancorata**](cim-docked.md) rappresenta la relazione tra due chassis. Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis). Questa relazione tipica è descritta in modo esplicito.

</dd> <dt>

[**\_ELEMENTCAPACITY CIM**](cim-elementcapacity.md)
</dt> <dd>

La classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associa un oggetto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici. Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.

</dd> <dt>

[**\_ELEMENTCONFIGURATION CIM**](cim-elementconfiguration.md)
</dt> <dd>

L'associazione [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) mette in correlazione un oggetto di [**\_ configurazione CIM**](cim-configuration.md) a uno o più elementi di sistema gestiti. L'oggetto di **\_ configurazione CIM** rappresenta un determinato comportamento o uno stato funzionale desiderato per il [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associato.

</dd> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

La classe [**CIM \_ ElementSetting**](cim-elementsetting.md) rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.

</dd> <dt>

[**\_ELEMENTSLINKED CIM**](cim-elementslinked.md)
</dt> <dd>

L'associazione [**CIM \_ ElementsLinked**](cim-elementslinked.md) rappresenta elementi fisici collegati da un collegamento fisico.

</dd> <dt>

[**\_ERRORCOUNTERSFORDEVICE CIM**](cim-errorcountersfordevice.md)
</dt> <dd>

La classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associa la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) al dispositivo logico a cui si applica.

</dd> <dt>

[**\_EXECUTEPROGRAM CIM**](cim-executeprogram.md)
</dt> <dd>

La classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) rappresenta i file che possono essere eseguiti nel sistema in cui è installato l'elemento software.

</dd> <dt>

[**\_Esportazione CIM**](cim-export.md)
</dt> <dd>

La classe di [**\_ esportazione CIM**](cim-export.md) rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio. Quando si esporta un intero file system, la directory deve fare riferimento alla directory più in alto della file system.

</dd> <dt>

[**\_EXTRACAPACITYGROUP CIM**](cim-extracapacitygroup.md)
</dt> <dd>

La classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) è derivata da un gruppo di ridondanza che indica che gli elementi aggregati hanno una capacità o una capacità superiore a quella necessaria. Un esempio di questo tipo di ridondanza è l'installazione di N + 1 alimentatori o ventilatori in un sistema.

</dd> <dt>

[**\_Ventola CIM**](cim-fan.md)
</dt> <dd>

La classe [**CIM \_ fan**](cim-fan.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento ventola.

</dd> <dt>

[**Azione filecim \_**](cim-fileaction.md)
</dt> <dd>

La classe [**CIM \_ fileaction**](cim-fileaction.md) consente all'autore di individuare i file già esistenti nel computer di un utente, quindi spostare o copiare tali file in una nuova posizione.

</dd> <dt>

[**Specifica del filecim \_**](cim-filespecification.md)
</dt> <dd>

La classe [**CIM \_ filespecification**](cim-filespecification.md) rappresenta un file che si trova in una posizione di sistema. Il file si trova nella directory identificata dall'associazione [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) . Il metodo [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa le informazioni per verificare l'esistenza del file. Si noti che le proprietà con un valore **null** non vengono controllate.

</dd> <dt>

[**Filestorage CIM \_**](cim-filestorage.md)
</dt> <dd>

L'associazione [**CIM \_ filestorage**](cim-filestorage.md) collega i file System e i file logici risolti tramite l'file System.

</dd> <dt>

[**\_File System CIM**](cim-filesystem.md)
</dt> <dd>

La classe [**CIM \_ filesystem**](cim-filesystem.md) rappresenta un file o un set di dati locale in un sistema di computer o montato in modalità remota da un file server.

</dd> <dt>

[**\_Piatto CIM**](cim-flatpanel.md)
</dt> <dd>

La classe [**CIM \_ piatto**](cim-flatpanel.md) rappresenta le funzionalità e la gestione del dispositivo logico del pannello flat.

</dd> <dt>

[**\_FROMDIRECTORYACTION CIM**](cim-fromdirectoryaction.md)
</dt> <dd>

L'associazione [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifica la directory di origine per l'azione del file. Quando si utilizza questa associazione, si presuppone che la directory di origine sia stata creata da un'azione precedente. Questa associazione non può esistere con un'associazione [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) ; un'azione file può coinvolgere solo una singola directory di origine.

</dd> <dt>

[**\_FROMDIRECTORYSPECIFICATION CIM**](cim-fromdirectoryspecification.md)
</dt> <dd>

L'associazione [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifica la directory di origine per l'azione del file. Quando si utilizza questa associazione, il presupposto è che la directory di origine esista già. Questa associazione non può esistere con un'associazione [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) ; un'azione file può coinvolgere solo una singola directory di origine.

</dd> <dt>

[**\_FRU CIM**](cim-fru.md)
</dt> <dd>

La classe [**CIM \_ FRU**](cim-fru.md) rappresenta una raccolta definita dal fornitore di prodotti ed elementi fisici associati a un'unità sostituibile sul campo (FRU) per supportare, gestire o aggiornare un prodotto nella posizione del cliente.

</dd> <dt>

[**\_FRUINCLUDESPRODUCT CIM**](cim-fruincludesproduct.md)
</dt> <dd>

La classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica che un'unità sostituibile sul campo (FRU) può essere costituita da altri prodotti.

</dd> <dt>

[**\_FRUPHYSICALELEMENTS CIM**](cim-fruphysicalelements.md)
</dt> <dd>

La classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) rappresenta gli elementi fisici che costituiscono un'unità sostituibile sul campo (FRU).

</dd> <dt>

[**\_HEATPIPE CIM**](cim-heatpipe.md)
</dt> <dd>

La classe [**CIM \_ HeatPipe**](cim-heatpipe.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento con pipe di calore.

</dd> <dt>

[**\_HOSTEDACCESSPOINT CIM**](cim-hostedaccesspoint.md)
</dt> <dd>

La classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito. Ogni sistema può ospitare molti SAP.

</dd> <dt>

[**\_HOSTEDBOOTSAP CIM**](cim-hostedbootsap.md)
</dt> <dd>

La classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) definisce il computer del sistema di hosting per una classe [**CIM \_ BootSAP**](cim-bootsap.md) . Poiché questa relazione è sottoclassata da [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), eredita lo schema di ambito/denominazione definito per [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md), in cui un punto di accesso rinvia al relativo sistema di hosting. In questo caso, **CIM \_ BootSAP** deve rinviare alla relativa classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) di hosting.

</dd> <dt>

[**\_HOSTEDBOOTSERVICE CIM**](cim-hostedbootservice.md)
</dt> <dd>

La classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associa un sistema di hosting e un servizio di avvio. Poiché questa relazione è sottoclassata da [**CIM \_ servizio ospitato**](cim-hostedservice.md), eredita lo schema di ambito/denominazione definito per il servizio, dove un servizio rinvia al relativo sistema di hosting.

</dd> <dt>

[**\_HOSTEDFILESYSTEM CIM**](cim-hostedfilesystem.md)
</dt> <dd>

L'associazione [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) rappresenta un collegamento tra il computer e i file System ospitati nel computer.

</dd> <dt>

[**\_HOSTEDJOBDESTINATION CIM**](cim-hostedjobdestination.md)
</dt> <dd>

La classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede. Un sistema può ospitare numerose code di processi. Le destinazioni dei processi rinviano al sistema host.

</dd> <dt>

[**\_Servizio ospitato CIM**](cim-hostedservice.md)
</dt> <dd>

La classe [**CIM \_ servizio ospitato**](cim-hostedservice.md) rappresenta un'associazione tra un servizio e il sistema in cui risiede la funzionalità. Un sistema può ospitare molti servizi, che rinviano al sistema host. Il modello non rappresenta servizi ospitati in più sistemi.

</dd> <dt>

[**\_INFRAREDCONTROLLER CIM**](cim-infraredcontroller.md)
</dt> <dd>

La classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) rappresenta le funzionalità e la gestione di un controller a infrarossi.

</dd> <dt>

[**CIM \_ installato**](cim-installedos.md)
</dt> <dd>

La classe di associazione [**CIM \_ installatoos**](cim-installedos.md) rappresenta un collegamento tra il computer e il sistema operativo installato. Un sistema operativo viene installato quando si trova in un ambito di archiviazione del computer (ad esempio, copiato in un'unità disco o scaricato in memoria).

</dd> <dt>

[**\_INSTALLEDSOFTWAREELEMENT CIM**](cim-installedsoftwareelement.md)
</dt> <dd>

La classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa un sistema di computer a un elemento software installato.

</dd> <dt>

[**\_IRQ CIM**](cim-irq.md)
</dt> <dd>

La classe [**CIM \_ IRQ**](cim-irq.md) rappresenta un IRQ (Intel Architecture interrupt request line).

</dd> <dt>

[**\_Processo CIM**](cim-job.md)
</dt> <dd>

La classe del [**\_ processo CIM**](cim-job.md) rappresenta un'unità di lavoro per un sistema, ad esempio un processo di stampa. Un processo è diverso da un processo perché è possibile pianificare un processo.

</dd> <dt>

[**\_JOBDESTINATION CIM**](cim-jobdestination.md)
</dt> <dd>

La classe [**CIM \_ JobDestination**](cim-jobdestination.md) rappresenta il punto in cui un processo viene inviato per l'elaborazione. Può fare riferimento a una coda che contiene zero o più processi, ad esempio una coda di stampa contenente processi di stampa. Le destinazioni dei processi sono ospitate in sistemi, in modo analogo al modo in cui i servizi sono ospitati nei sistemi.

</dd> <dt>

[**\_JOBDESTINATIONJOBS CIM**](cim-jobdestinationjobs.md)
</dt> <dd>

L'associazione [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) descrive la posizione di invio di un processo per l'elaborazione, ovvero la destinazione del processo.

</dd> <dt>

[**\_Tastiera CIM**](cim-keyboard.md)
</dt> <dd>

La classe [**CIM \_ Keyboard**](cim-keyboard.md) rappresenta le funzionalità e la gestione del dispositivo logico da tastiera.

</dd> <dt>

[**\_LINKHASCONNECTOR CIM**](cim-linkhasconnector.md)
</dt> <dd>

La classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa i cavi e i collegamenti usati come connettori fisici, che connettono gli elementi fisici. Questa associazione definisce in modo esplicito la relazione dei connettori per [**CIM \_ PhysicalLink**](cim-physicallink.md).

</dd> <dt>

[**\_LOCALFILESYSTEM CIM**](cim-localfilesystem.md)
</dt> <dd>

La classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) rappresenta l'archivio file controllato da un sistema di computer tramite mezzi locali, ad esempio l'accesso diretto ai driver di dispositivo. L'archivio file può essere gestito direttamente dal computer, senza la necessità che un altro computer funga da file server. Per un file system cluster, tuttavia, il file system è locale e, di conseguenza, rinvia al cluster.

</dd> <dt>

[**\_Percorso CIM**](cim-location.md)
</dt> <dd>

La classe del [**\_ percorso CIM**](cim-location.md) rappresenta la posizione e l'indirizzo di un elemento fisico.

</dd> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dd>

La classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) rappresenta un'entità hardware che può essere o meno realizzata nell'hardware fisico.

</dd> <dt>

[**\_Disco logico CIM**](cim-logicaldisk.md)
</dt> <dd>

La classe [**CIM \_ disco logico**](cim-logicaldisk.md) rappresenta un intervallo contiguo di blocchi logici identificabili da un file System tramite il campo **DeviceID** (Key) del disco. Ad esempio, in un ambiente Windows, il campo **DeviceID** contiene una lettera di unità; in un ambiente UNIX, contiene il percorso di accesso; e in un ambiente NetWare contiene il nome del volume.

</dd> <dt>

[**\_LOGICALDISKBASEDONPARTITION CIM**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

La classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associa un disco logico con la partizione del disco in cui risiede.

</dd> <dt>

[**\_LOGICALDISKBASEDONVOLUMESET CIM**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

L'associazione [**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) mette in relazione i dischi logici con il volume in cui sono stati trovati. I dischi logici possono essere basati su un singolo volume, ad esempio esposto da un responsabile del volume software, o una partizione disco.

</dd> <dt>

[**\_LogicalElement CIM**](cim-logicalelement.md)
</dt> <dd>

La classe [**CIM \_ LogicalElement**](cim-logicalelement.md) è la classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità del sistema, sotto forma di dispositivi logici.

</dd> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> <dd>

La classe [**CIM \_ LogicalFile**](cim-logicalfile.md) rappresenta una raccolta denominata di dati, che può essere un codice eseguibile, che si trova in un file System in un extent di archiviazione.

</dd> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dd>

La classe [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.

</dd> <dt>

[**\_MAGNETOOPTICALDRIVE CIM**](cim-magnetoopticaldrive.md)
</dt> <dd>

La classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) rappresenta le funzionalità e la gestione di un'unità magneto-ottico, un sottotipo del dispositivo di accesso multimediale.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

La classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) è la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.

</dd> <dt>

[**\_MANAGEMENTCONTROLLER CIM**](cim-managementcontroller.md)
</dt> <dd>

La classe [**CIM \_ ManagementController**](cim-managementcontroller.md) è correlata alle funzionalità e alla gestione di un controller di gestione.

</dd> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> <dd>

La classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) rappresenta la possibilità di accedere a uno o più supporti e quindi di usare il supporto per archiviare e recuperare i dati.

</dd> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dd>

L'associazione [**CIM \_ MediaPresent**](cim-mediapresent.md) descrive una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.

</dd> <dt>

[**\_Memoria CIM**](cim-memory.md)
</dt> <dd>

La classe [**CIM \_ Memory**](cim-memory.md) rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.

</dd> <dt>

[**\_MEMORYCAPACITY CIM**](cim-memorycapacity.md)
</dt> <dd>

La classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) rappresenta la memoria che può essere installata su un elemento fisico e le configurazioni minime e massime. Le informazioni sulla memoria attualmente installata e i requisiti minimi e massimi di un elemento si trovano nelle istanze della classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .

</dd> <dt>

[**\_MEMORYCHECK CIM**](cim-memorycheck.md)
</dt> <dd>

La classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) specifica una condizione per la quantità minima di memoria che deve essere disponibile in un sistema.

</dd> <dt>

[**\_MEMORYMAPPEDIO CIM**](cim-memorymappedio.md)
</dt> <dd>

La classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) rappresenta l'I/O mappato alla memoria dell'architettura del computer. Questa classe indirizza le risorse di memoria e di I/O della porta.

</dd> <dt>

[**\_MEMORYONCARD CIM**](cim-memoryoncard.md)
</dt> <dd>

La classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa la memoria fisica che si trova sulle lavagne di hosting, schede scheda e così via. Questa associazione definisce in modo esplicito la relazione di memoria con le schede.

</dd> <dt>

[**\_MEMORYWITHMEDIA CIM**](cim-memorywithmedia.md)
</dt> <dd>

La classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.

</dd> <dt>

[**\_MODIFYSETTINGACTION CIM**](cim-modifysettingaction.md)
</dt> <dd>

La classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) rappresenta le informazioni per la modifica di un file di impostazioni specifico, per una voce specifica, con un valore specifico.

</dd> <dt>

[**\_MONITORRESOLUTION CIM**](cim-monitorresolution.md)
</dt> <dd>

La classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) rappresenta la relazione tra risoluzioni orizzontali e verticali e la frequenza di aggiornamento e la modalità di analisi per un monitor desktop. I valori vengono specificati nell'oggetto controller video.

</dd> <dt>

[**\_MONITORSETTING CIM**](cim-monitorsetting.md)
</dt> <dd>

La classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associa la risoluzione del monitoraggio al monitor desktop a cui si applica.

</dd> <dt>

[**\_Montaggio CIM**](cim-mount.md)
</dt> <dd>

La classe di [**\_ montaggio CIM**](cim-mount.md) rappresenta un'associazione tra un file System e una directory a cui è collegata.

</dd> <dt>

[**\_MULTISTATESENSOR CIM**](cim-multistatesensor.md)
</dt> <dd>

La classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) rappresenta un set di sensori binari a più membri in cui ogni sensore binario segnala un risultato booleano.

</dd> <dt>

[**\_NETWORKADAPTER CIM**](cim-networkadapter.md)
</dt> <dd>

La classe [**CIM \_ NetworkAdapter**](cim-networkadapter.md) è una classe astratta che definisce i concetti relativi all'hardware di rete generale, ad esempio l'indirizzo permanente o la velocità dell'operazione. Le informazioni vengono trasmesse mediante l'associazione [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .

</dd> <dt>

[**\_NFS CIM**](cim-nfs.md)
</dt> <dd>

La classe [**CIM \_ NFS**](cim-nfs.md) rappresenta una file system remota montata usando il protocollo di rete file System (NFS), da un sistema di computer.

</dd> <dt>

[**\_NONVOLATILESTORAGE CIM**](cim-nonvolatilestorage.md)
</dt> <dd>

La classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) rappresenta le funzionalità e la gestione di risorse di archiviazione non volatili. La memoria non volatile include in modo nativo archiviazione flash e ROM.

</dd> <dt>

[**\_NUMERICSENSOR CIM**](cim-numericsensor.md)
</dt> <dd>

La classe [**CIM \_ NumericSensor**](cim-numericsensor.md) rappresenta un sensore numerico che restituisce letture numeriche e, facoltativamente, supporta le impostazioni di soglia.

</dd> <dt>

[**\_OPERATINGSYSTEM CIM**](cim-operatingsystem.md)
</dt> <dd>

La classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) rappresenta un sistema operativo del computer, costituito da software e firmware che rendono utilizzabile l'hardware di un sistema di computer.

</dd> <dt>

[**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

La classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) rappresenta le funzionalità software che costituiscono il sistema operativo.

</dd> <dt>

[**\_OSPROCESS CIM**](cim-osprocess.md)
</dt> <dd>

La classe [**CIM \_ OSProcess**](cim-osprocess.md) associa il sistema operativo e uno o più processi in esecuzione nel contesto del sistema operativo.

</dd> <dt>

[**\_OSVERSIONCHECK CIM**](cim-osversioncheck.md)
</dt> <dd>

La classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) specifica le versioni del sistema operativo in grado di supportare un elemento software.

</dd> <dt>

[**\_PACKAGEALARM CIM**](cim-packagealarm.md)
</dt> <dd>

L'associazione [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) rappresenta la relazione in cui viene installato un dispositivo di allarme come parte di un pacchetto. L'installazione indica i problemi con l'ambiente del pacchetto, ovvero il relativo stato di sicurezza o l'integrità generale.

</dd> <dt>

[**\_PACKAGECOOLING CIM**](cim-packagecooling.md)
</dt> <dd>

L'associazione [**CIM \_ PackageCooling**](cim-packagecooling.md) rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.

</dd> <dt>

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> <dd>

L'associazione [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.

</dd> <dt>

[**\_PACKAGEINCHASSIS CIM**](cim-packageinchassis.md)
</dt> <dd>

L'associazione [**CIM \_ PackageInChassis**](cim-packageinchassis.md) rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.

</dd> <dt>

[**\_PACKAGEINSLOT CIM**](cim-packageinslot.md)
</dt> <dd>

L'associazione [**CIM \_ PackageInSlot**](cim-packageinslot.md) rappresenta la relazione tra le schede dispositivo e lo chassis in cui sono montate.

</dd> <dt>

[**\_PACKAGETEMPSENSOR CIM**](cim-packagetempsensor.md)
</dt> <dd>

L'associazione [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) rappresenta la relazione in cui un sensore di temperatura viene spesso installato in un pacchetto, ad esempio uno chassis o un rack, per monitorare l'ambiente del pacchetto.

</dd> <dt>

[**\_PARALLELCONTROLLER CIM**](cim-parallelcontroller.md)
</dt> <dd>

L'associazione [**CIM \_ ParallelController**](cim-parallelcontroller.md) è correlata alle funzionalità e alla gestione del dispositivo logico della porta parallela.

</dd> <dt>

[**\_PARTICIPATESINSET CIM**](cim-participatesinset.md)
</dt> <dd>

La classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica gli elementi fisici che devono essere sostituiti insieme.

</dd> <dt>

[**\_PCICONTROLLER CIM**](cim-pcicontroller.md)
</dt> <dd>

La classe [**CIM \_ PCIController**](cim-pcicontroller.md) rappresenta le proprietà e la gestione di un controller PCI. Le proprietà di questa classe e delle relative sottoclassi sono definite nelle diverse specifiche PCI pubblicate da PCI SIG.

</dd> <dt>

[**\_PCMCIACONTROLLER CIM**](cim-pcmciacontroller.md)
</dt> <dd>

La classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) rappresenta le funzionalità e la gestione di un controller PCMCIA (Personal Computer Memory Card International Association).

</dd> <dt>

[**\_PCVIDEOCONTROLLER CIM**](cim-pcvideocontroller.md)
</dt> <dd>

Il [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) rappresenta le funzionalità e la gestione di un personal computer controller video, un sottotipo di un controller video.

</dd> <dt>

[**\_PEXTENTREDUNDANCYCOMPONENT CIM**](cim-pextentredundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) rappresenta gli extent fisici che fanno parte di un gruppo di ridondanza di archiviazione.

</dd> <dt>

[**\_PHYSICALCAPACITY CIM**](cim-physicalcapacity.md)
</dt> <dd>

La classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) è una classe astratta che rappresenta i requisiti minimi e massimi di un elemento fisico e la capacità di supportare diversi tipi di hardware. Ad esempio, è possibile modellare i requisiti di memoria minimi e massimi come sottoclasse di **CIM \_ PhysicalCapacity**.

</dd> <dt>

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> <dd>

La classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) rappresenta un componente di base o di basso livello all'interno di un pacchetto. Un elemento fisico che non è un collegamento, un connettore o un pacchetto è un discendente (o membro) di questa classe.

</dd> <dt>

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> <dd>

La classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) rappresenta qualsiasi elemento fisico usato per connettersi ad altri elementi. Qualsiasi oggetto in grado di connettersi e trasmettere segnali o potere tra due o più elementi fisici è un discendente (o membro) di questa classe.

</dd> <dt>

[**\_PhysicalElement CIM**](cim-physicalelement.md)
</dt> <dd>

Le sottoclassi [**CIM \_ PhysicalElement**](cim-physicalelement.md) definiscono qualsiasi componente di un sistema con un'identità fisica distinta. Le istanze di questa classe possono essere definite in termini di etichette che possono essere fisicamente collegate all'oggetto.

</dd> <dt>

[**\_PHYSICALELEMENTLOCATION CIM**](cim-physicalelementlocation.md)
</dt> <dd>

La classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associa un elemento fisico a un [**oggetto \_ percorso CIM**](cim-location.md) a scopo di inventario o sostituzione.

</dd> <dt>

[**\_PHYSICALEXTENT CIM**](cim-physicalextent.md)
</dt> <dd>

La classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) rappresenta un'implementazione RAID di SCC. Definisce gli indirizzi di blocco indirizzabili consecutivi in un singolo dispositivo di archiviazione che vengono considerati come un singolo extent di archiviazione nella stessa classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) . In alternativa, quando si usa la configurazione automatica, è possibile creare un'istanza o estendere la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .

</dd> <dt>

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> <dd>

La classe [**CIM \_ PhysicalFrame**](cim-physicalframe.md) è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione. In questa classe padre sono incluse proprietà quali **VisibleAlarm** e **AudibleAlarm** e i dati relativi alle violazioni della sicurezza.

</dd> <dt>

[**\_PHYSICALLINK CIM**](cim-physicallink.md)
</dt> <dd>

La classe [**CIM \_ PhysicalLink**](cim-physicallink.md) rappresenta il cablaggio di elementi fisici.

</dd> <dt>

[**\_PHYSICALMEDIA CIM**](cim-physicalmedia.md)
</dt> <dd>

La classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via.

</dd> <dt>

[**\_PHYSICALMEMORY CIM**](cim-physicalmemory.md)
</dt> <dd>

La classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) rappresenta dispositivi di memoria di basso livello, ad esempio SIMM, DIMM, chip di memoria RAW e così via.

</dd> <dt>

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> <dd>

La classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) rappresenta elementi fisici che contengono o ospitano altri componenti. Gli esempi sono un'enclosure rack o una scheda scheda.

</dd> <dt>

[**\_POINTINGDEVICE CIM**](cim-pointingdevice.md)
</dt> <dd>

La classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) rappresenta un dispositivo che punta alle aree sullo schermo. Qualsiasi dispositivo che manipola un puntatore o punta a aree in una visualizzazione visiva è un membro di questa classe. Ad esempio mouse, stilo, touch pad o tablet.

</dd> <dt>

[**\_POTSMODEM CIM**](cim-potsmodem.md)
</dt> <dd>

La classe [**CIM \_ POTSModem**](cim-potsmodem.md) rappresenta un dispositivo che converte i dati binari in modulazioni Wave per la trasmissione basata su audio connettendosi alla rete Plain Old Phone System (POTS).

</dd> <dt>

[**\_Alimentatore CIM**](cim-powersupply.md)
</dt> <dd>

La classe [**CIM \_ alimentatore**](cim-powersupply.md) rappresenta le funzionalità e la gestione del dispositivo logico dell'alimentatore.

</dd> <dt>

[**\_Stampante CIM**](cim-printer.md)
</dt> <dd>

La classe [**CIM \_ Printer**](cim-printer.md) rappresenta le funzionalità e la gestione del dispositivo logico Printer.

</dd> <dt>

[**\_Processo CIM**](cim-process.md)
</dt> <dd>

La classe di [**\_ processo CIM**](cim-process.md) rappresenta una singola istanza di un programma in esecuzione. Un utente visualizza in genere un processo come un'applicazione o un'attività.

</dd> <dt>

[**\_PROCESSEXECUTABLE CIM**](cim-processexecutable.md)
</dt> <dd>

La classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) rappresenta un collegamento tra un processo e un file di dati e indica che il file partecipa all'esecuzione del processo.

</dd> <dt>

[**\_Processore CIM**](cim-processor.md)
</dt> <dd>

La classe del [**\_ processore CIM**](cim-processor.md) rappresenta le funzionalità e la gestione del dispositivo logico del processore.

</dd> <dt>

[**\_PROCESSTHREAD CIM**](cim-processthread.md)
</dt> <dd>

La classe [**CIM \_ ProcessThread**](cim-processthread.md) rappresenta un collegamento tra un processo e i thread in esecuzione nel contesto del processo.

</dd> <dt>

[**\_Prodotto CIM**](cim-product.md)
</dt> <dd>

La classe di [**\_ prodotto CIM**](cim-product.md) è una classe concreta che rappresenta una raccolta di elementi fisici, funzionalità software e altri prodotti, acquisiti come unità. L'acquisizione implica un accordo tra il fornitore e il consumer, che può avere implicazioni sulla licenza, il supporto e la garanzia di prodotti.

</dd> <dt>

[**\_PRODUCTFRU CIM**](cim-productfru.md)
</dt> <dd>

La classe [**CIM \_ ProductFRU**](cim-productfru.md) rappresenta un'associazione tra il prodotto e un'unità sostituibile sul campo (FRU), che fornisce informazioni sui componenti del prodotto che sono stati o sono stati sostituiti.

</dd> <dt>

[**\_PRODUCTPARENTCHILD CIM**](cim-productparentchild.md)
</dt> <dd>

L'associazione [**CIM \_ ProductParentChild**](cim-productparentchild.md) definisce una gerarchia padre-figlio tra i prodotti. Ad esempio, un prodotto può essere fornito con altri prodotti.

</dd> <dt>

[**\_PRODUCTPHYSICALELEMENTS CIM**](cim-productphysicalelements.md)
</dt> <dd>

La classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) rappresenta gli elementi fisici che costituiscono un prodotto.

</dd> <dt>

[**\_PRODUCTPRODUCTDEPENDENCY CIM**](cim-productproductdependency.md)
</dt> <dd>

La classe [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) rappresenta un'associazione tra due prodotti, che indica che è necessario installare o assente per il funzionamento dell'altro. Questa operazione è concettualmente equivalente all'associazione [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .

</dd> <dt>

[**\_PRODUCTSOFTWAREFEATURES CIM**](cim-productsoftwarefeatures.md)
</dt> <dd>

L'associazione [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica le funzionalità software per un determinato prodotto.

</dd> <dt>

[**\_PRODUCTSUPPORT CIM**](cim-productsupport.md)
</dt> <dd>

La classe [**CIM \_ ProductSupport**](cim-productsupport.md) rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto. Sono disponibili vari tipi di supporto per un prodotto; lo stesso oggetto di supporto può fornire assistenza per più prodotti.

</dd> <dt>

[**\_PROTECTEDSPACEEXTENT CIM**](cim-protectedspaceextent.md)
</dt> <dd>

La classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) rappresenta indirizzi di blocco logico indirizzabili, che vengono trattati come un singolo extent di archiviazione, ma si trovano in un singolo extent fisico.

</dd> <dt>

[**\_PSEXTENTBASEDONPEXTENT CIM**](cim-psextentbasedonpextent.md)
</dt> <dd>

La classe [**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa gli extent dello spazio protetto basati su un extent fisico.

</dd> <dt>

[**\_Rack CIM**](cim-rack.md)
</dt> <dd>

La classe [**CIM \_ rack**](cim-rack.md) rappresenta un rack (un frame fisico o un'enclosure) in cui vengono archiviati gli chassis. In genere, un rack rappresenta l'enclosure; tutti i componenti funzionanti sono inclusi nello chassis.

</dd> <dt>

[**CIM \_ realizza**](cim-realizes.md)
</dt> <dd>

La classe [**CIM \_ realizza**](cim-realizes.md) la classe che rappresenta l'associazione che definisce il mapping tra un dispositivo logico e il componente fisico che implementa il dispositivo.

</dd> <dt>

[**\_REALIZESAGGREGATEPEXTENT CIM**](cim-realizesaggregatepextent.md)
</dt> <dd>

L'associazione [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) rappresenta la relazione in cui la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) è realizzata su un supporto fisico.

</dd> <dt>

[**\_REALIZESDISKPARTITION CIM**](cim-realizesdiskpartition.md)
</dt> <dd>

La classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) rappresenta una partizione disco su un supporto fisico che modella la creazione di partizioni in un'unità IDE o SCSI non elaborata.

</dd> <dt>

[**\_REALIZESPEXTENT CIM**](cim-realizespextent.md)
</dt> <dd>

L'associazione [**CIM \_ RealizesPExtent**](cim-realizespextent.md) rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico. Inoltre, viene specificato l'indirizzo iniziale dell'extent fisico sul supporto fisico.

</dd> <dt>

[**\_REBOOTACTION CIM**](cim-rebootaction.md)
</dt> <dd>

La classe [**CIM \_ rebootaction**](cim-rebootaction.md) causa un riavvio del sistema in cui è installato l'elemento software.

</dd> <dt>

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associa un gruppo di ridondanza composto da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono la ridondanza. Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.

</dd> <dt>

[**\_REDUNDANCYGROUP CIM**](cim-redundancygroup.md)
</dt> <dd>

La classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) rappresenta una raccolta di elementi di sistema gestiti, che indica che i componenti aggregati, insieme, forniscono la ridondanza. Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.

</dd> <dt>

[**\_Refrigerazione CIM**](cim-refrigeration.md)
</dt> <dd>

La classe di [**\_ refrigerazione CIM**](cim-refrigeration.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento a freddo.

</dd> <dt>

[**\_RELATEDSTATISTICS CIM**](cim-relatedstatistics.md)
</dt> <dd>

L'associazione [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) rappresenta gerarchie e dipendenze di classi [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) correlate.

</dd> <dt>

[**\_REMOTEFILESYSTEM CIM**](cim-remotefilesystem.md)
</dt> <dd>

La classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) rappresenta una file system remota a cui si accede tramite un servizio correlato alla rete. In questo caso, l'archivio file è ospitato da un computer che funge da file server.

</dd> <dt>

[**\_REMOVEDIRECTORYACTION CIM**](cim-removedirectoryaction.md)
</dt> <dd>

La classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) rimuove le directory per gli elementi software.

</dd> <dt>

[**\_REMOVEFILEACTION CIM**](cim-removefileaction.md)
</dt> <dd>

La classe [**CIM \_ RemoveFileAction**](cim-removefileaction.md) Disinstalla i file.

</dd> <dt>

[**\_REPLACEMENTSET CIM**](cim-replacementset.md)
</dt> <dd>

La classe [**CIM \_ ReplacementSet**](cim-replacementset.md) aggrega gli elementi fisici che devono essere sostituiti insieme. Ad esempio, quando si sostituisce una scheda di memoria, è possibile rimuovere e sostituire anche i chip di memoria del componente. In alternativa, è possibile usare questa associazione per sostituire o aggiornare un set di chip di memoria.

</dd> <dt>

[**\_RESIDESONEXTENT CIM**](cim-residesonextent.md)
</dt> <dd>

La classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) rappresenta un'associazione tra un file System e l'extent di archiviazione in cui si trova. In genere, un file system risiede su un disco logico.

</dd> <dt>

[**CIM \_ in esecuzione**](cim-runningos.md)
</dt> <dd>

La classe [**CIM \_ RunningOS**](cim-runningos.md) rappresenta il sistema operativo attualmente in esecuzione. Al massimo, un sistema operativo può essere eseguito in qualsiasi momento in un computer. il computer potrebbe non essere attualmente avviato o il sistema operativo potrebbe essere sconosciuto.

</dd> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> <dd>

La classe [**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md) è un'associazione tra due punti di accesso al servizio (SAP), che indica che il secondo SAP è necessario affinché il primo SAP si connetta con il servizio.

</dd> <dt>

[**\_Scanner CIM**](cim-scanner.md)
</dt> <dd>

Lo [**\_ scanner CIM**](cim-scanner.md) rappresenta le funzionalità e la gestione del dispositivo logico dello scanner.

</dd> <dt>

[**\_Controller SCSI CIM**](cim-scsicontroller.md)
</dt> <dd>

La classe [**CIM \_ controller SCSI**](cim-scsicontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico del controller SCSI.

</dd> <dt>

[**\_SCSIINTERFACE CIM**](cim-scsiinterface.md)
</dt> <dd>

rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite un controller SCSI e le caratteristiche di accesso.

</dd> <dt>

[**\_Sensore CIM**](cim-sensor.md)
</dt> <dd>

La classe del [**\_ sensore CIM**](cim-sensor.md) rappresenta un dispositivo hardware in grado di misurare le caratteristiche di una proprietà fisica, ad esempio le caratteristiche di temperatura o di tensione di un sistema di computer.

</dd> <dt>

[**\_Controller seriale CIM**](cim-serialcontroller.md)
</dt> <dd>

La classe [**CIM \_ controller seriale**](cim-serialcontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico della porta seriale.

</dd> <dt>

[**\_SERIALINTERFACE CIM**](cim-serialinterface.md)
</dt> <dd>

La classe [**CIM \_ SerialInterface**](cim-serialinterface.md) rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.

</dd> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> <dd>

La classe del [**\_ servizio CIM**](cim-service.md) rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o del software. Un servizio è un oggetto generico per la configurazione e la gestione dell'implementazione di funzionalità. non si tratta della funzionalità stessa.

</dd> <dt>

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> <dd>

La classe di associazione [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) rappresenta i punti di accesso per un servizio. Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.

</dd> <dt>

[**\_SERVICEACCESSPOINT CIM**](cim-serviceaccesspoint.md)
</dt> <dd>

La classe [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) rappresenta la possibilità di usare o richiamare un servizio. I punti di accesso rappresentano i servizi disponibili per l'utilizzo da altre entità.

</dd> <dt>

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> <dd>

La classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP), che indica che il servizio SAP a cui viene fatto riferimento viene usato dal servizio per fornire le funzionalità.

</dd> <dt>

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dd>

La classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) rappresenta un'associazione tra due servizi.

</dd> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dd>

La classe di [**\_ Impostazioni CIM**](cim-setting.md) rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.

</dd> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> <dd>

La classe [**CIM \_ SettingCheck**](cim-settingcheck.md) specifica le informazioni necessarie per controllare un determinato file di impostazioni per una voce specifica che contiene un valore uguale al valore specificato. Si presuppone che non venga fatta distinzione tra maiuscole e minuscole.

</dd> <dt>

[**\_SETTINGCONTEXT CIM**](cim-settingcontext.md)
</dt> <dd>

La classe [**CIM \_ SettingContext**](cim-settingcontext.md) associa gli oggetti di configurazione a oggetti setting.

</dd> <dt>

[**\_Slot CIM**](cim-slot.md)
</dt> <dd>

La classe di [**\_ slot CIM**](cim-slot.md) rappresenta i connettori in cui vengono inseriti i pacchetti.

</dd> <dt>

[**\_SLOTINSLOT CIM**](cim-slotinslot.md)
</dt> <dd>

La relazione [**CIM \_ SlotInSlot**](cim-slotinslot.md) rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting.

</dd> <dt>

[**\_Software CIM**](cim-softwareelement.md)
</dt> <dd>

La classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) scompone un oggetto [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) in un set di parti gestibili o distribuibile singolarmente per una determinata piattaforma. La piattaforma di un elemento software viene identificata in modo univoco dall'architettura hardware e dal sistema operativo sottostanti.

</dd> <dt>

[**\_SOFTWAREELEMENTACTIONS CIM**](cim-softwareelementactions.md)
</dt> <dd>

L'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifica le azioni per un elemento software.

</dd> <dt>

[**\_SOFTWAREELEMENTCHECKS CIM**](cim-softwareelementchecks.md)
</dt> <dd>

La classe di associazione [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.

</dd> <dt>

[**\_SOFTWAREELEMENTVERSIONCHECK CIM**](cim-softwareelementversioncheck.md)
</dt> <dd>

La classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) rappresenta un tipo di elemento software che deve esistere nell'ambiente.

</dd> <dt>

[**\_SoftwareFeature CIM**](cim-softwarefeature.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) rappresenta una funzione o una funzionalità specifica di un prodotto o di un sistema applicativo.

</dd> <dt>

[**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software.

</dd> <dt>

[**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) rappresenta un'associazione tra un servizio e il modo in cui viene implementata nel software.

</dd> <dt>

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

L'associazione [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica gli elementi software che costituiscono una funzionalità software specifica.

</dd> <dt>

[**\_SPAREGROUP CIM**](cim-sparegroup.md)
</dt> <dd>

La classe [**CIM \_ SpareGroup**](cim-sparegroup.md) è derivata dalla classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica che uno o più elementi aggregati possono essere risparmiati.

</dd> <dt>

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> <dd>

La classe [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) è una classe radice per la raccolta arbitraria di dati statistici o metriche applicabili a uno o più elementi di sistema gestiti.

</dd> <dt>

[**\_Statistiche CIM**](cim-statistics.md)
</dt> <dd>

La classe [**CIM \_ Statistics**](cim-statistics.md) rappresenta un'associazione che mette in correlazione gli elementi di sistema gestiti ai gruppi statistici che vi si applicano.

</dd> <dt>

[**\_STORAGEDEFECT CIM**](cim-storagedefect.md)
</dt> <dd>

L'aggregazione [**CIM \_ StorageDefect**](cim-storagedefect.md) raccoglie gli errori di archiviazione per un extent di archiviazione.

</dd> <dt>

[**\_STORAGEERROR CIM**](cim-storageerror.md)
</dt> <dd>

La classe [**CIM \_ StorageError**](cim-storageerror.md) rappresenta i blocchi di supporti o di spazio di memoria di cui è stato eseguito il mapping fuori uso a causa di errori. La chiave della classe è la proprietà **IndirizzoIniziale** dei byte in errore.

</dd> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> <dd>

La classe [**CIM \_ StorageExtent**](cim-storageextent.md) rappresenta le funzionalità e la gestione dei diversi supporti esistenti per archiviare i dati e consentire il recupero dei dati. Questa classe padre può rappresentare i vari componenti di RAID (hardware o software) o un'estensione logica non elaborata in un supporto fisico.

</dd> <dt>

[**\_STORAGEREDUNDANCYGROUP CIM**](cim-storageredundancygroup.md)
</dt> <dd>

La classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) rappresenta informazioni di ridondanza relative all'archiviazione di massa.

</dd> <dt>

[**\_SUPPORTACCESS CIM**](cim-supportaccess.md)
</dt> <dd>

La classe [**CIM \_ SupportAccess**](cim-supportaccess.md) definisce come ottenere assistenza per un prodotto.

</dd> <dt>

[**\_SWAPSPACECHECK CIM**](cim-swapspacecheck.md)
</dt> <dd>

La classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) specifica la quantità di spazio di swapping che deve essere disponibile nel sistema.

</dd> <dt>

[**\_Sistema CIM**](cim-system.md)
</dt> <dd>

La classe di [**\_ sistema CIM**](cim-system.md) aggrega un set enumerabile di elementi di sistema gestiti. L'aggregazione funziona come un intero funzionale. All'interno di una sottoclasse particolare del sistema è presente un elenco ben definito di classi di elementi di sistema gestite le cui istanze devono essere aggregate.

</dd> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dd>

classe di associazione Common Information Model (CIM) che stabilisce le relazioni tra un sistema e gli elementi del sistema gestito di cui è composto.

</dd> <dt>

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dd>

L'associazione [**CIM \_ SystemDevice**](cim-systemdevice.md) rappresenta una relazione esplicita in cui i dispositivi logici possono essere aggregati da un sistema.

</dd> <dt>

[**\_SYSTEMRESOURCE CIM**](cim-systemresource.md)
</dt> <dd>

La classe [**CIM \_ SystemResource**](cim-systemresource.md) rappresenta un'entità gestita dal BIOS o un sistema operativo che è disponibile per l'uso da parte di software e dispositivi logici.

</dd> <dt>

[**\_Contagiri CIM**](cim-tachometer.md)
</dt> <dd>

La classe [**CIM \_ contagiri**](cim-tachometer.md) esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**\_TAPEDRIVE CIM**](cim-tapedrive.md)
</dt> <dd>

La classe [**CIM \_ TapeDrive**](cim-tapedrive.md) rappresenta un'unità nastro nel sistema. Le unità nastro si distinguono principalmente in quanto è possibile accedervi solo in modo sequenziale.

</dd> <dt>

[**\_Sensore CIM**](cim-temperaturesensor.md)
</dt> <dd>

La classe [**CIM \_ sensore**](cim-temperaturesensor.md) esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.

</dd> <dt>

[**\_Thread CIM**](cim-thread.md)
</dt> <dd>

La classe di [**\_ thread CIM**](cim-thread.md) rappresenta la possibilità di eseguire unità di un processo o di un'attività, in parallelo. Un processo può avere molti thread, ognuno dei quali è debole per il processo.

</dd> <dt>

[**\_TODIRECTORYACTION CIM**](cim-todirectoryaction.md)
</dt> <dd>

L'associazione [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifica la directory di destinazione per l'azione del file.

</dd> <dt>

[**\_TODIRECTORYSPECIFICATION CIM**](cim-todirectoryspecification.md)
</dt> <dd>

L'associazione [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica la directory di destinazione per l'azione del file.

</dd> <dt>

[**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

La classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) rappresenta le funzionalità e la gestione di un gruppo di continuità (UPS, Power Supply).

</dd> <dt>

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dd>

La classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) rappresenta un computer desktop, mobile, di rete, un server o un altro tipo di computer a nodo singolo.

</dd> <dt>

[**\_USBCONTROLLER CIM**](cim-usbcontroller.md)
</dt> <dd>

La classe [**CIM \_ USBController**](cim-usbcontroller.md) rappresenta le funzionalità e la gestione di un controller USB.

</dd> <dt>

[**\_USBCONTROLLERHASHUB CIM**](cim-usbcontrollerhashub.md)
</dt> <dd>

La classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) definisce gli hub a valle del controller USB.

</dd> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> <dd>

La classe [**CIM \_ usbdevice**](cim-usbdevice.md) rappresenta le caratteristiche di gestione di un dispositivo USB.

</dd> <dt>

[**\_Usbhub CIM**](cim-usbhub.md)
</dt> <dd>

La classe [**CIM \_ USBHub**](cim-usbhub.md) rappresenta le funzionalità e la gestione di un hub USB.

</dd> <dt>

[**\_USERDEVICE CIM**](cim-userdevice.md)
</dt> <dd>

La classe [**CIM \_ UserDevice**](cim-userdevice.md) è una classe padre da cui discendono altre classi, ad esempio [**CIM \_ Keyboard**](cim-keyboard.md) o [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md). I dispositivi utente sono dispositivi logici che consentono all'utente di un sistema informatico di immettere, visualizzare o ascoltare i dati.

</dd> <dt>

[**\_VERSIONCOMPATIBILITYCHECK CIM**](cim-versioncompatibilitycheck.md)
</dt> <dd>

La classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) specifica se è consentito creare lo stato successivo di un elemento software.

</dd> <dt>

[**\_VIDEOBIOSELEMENT CIM**](cim-videobioselement.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.

</dd> <dt>

[**\_VIDEOBIOSFEATURE CIM**](cim-videobiosfeature.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) rappresenta le funzionalità del software di basso livello utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.

</dd> <dt>

[**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa una funzionalità BIOS video e i relativi elementi BIOS video aggregati.

</dd> <dt>

[**\_VIDEOCONTROLLER CIM**](cim-videocontroller.md)
</dt> <dd>

La classe [**CIM \_ VideoController**](cim-videocontroller.md) rappresenta le funzionalità e la gestione del controller video.

</dd> <dt>

[**\_VIDEOCONTROLLERRESOLUTION CIM**](cim-videocontrollerresolution.md)
</dt> <dd>

La classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) rappresenta le varie modalità video che un controller video può supportare.

</dd> <dt>

[**\_VIDEOSETTING CIM**](cim-videosetting.md)
</dt> <dd>

La classe [**CIM \_ VideoSetting**](cim-videosetting.md) associa l'oggetto impostazione [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) al controller a cui si applica.

</dd> <dt>

[**\_VOLATILESTORAGE CIM**](cim-volatilestorage.md)
</dt> <dd>

La classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) rappresenta le funzionalità e la gestione dell'archiviazione volatile.

</dd> <dt>

[**\_Sensore CIM**](cim-voltagesensor.md)
</dt> <dd>

La classe [**CIM \_ sensore**](cim-voltagesensor.md) esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM. Con aggiunte alle classi CIM [**\_ Sensor**](cim-sensor.md) e [**cim \_ NumericSensor**](cim-numericsensor.md) nella versione 2,2, non è più necessario.

</dd> <dt>

[**\_Volume del volume CIM**](cim-volumeset.md)
</dt> <dd>

La classe [**CIM \_ volumet**](cim-volumeset.md) rappresenta un intervallo contiguo di blocchi logici presentati all'ambiente operativo per la lettura e la scrittura di dati utente.

</dd> <dt>

[**\_Wormdrive CIM**](cim-wormdrive.md)
</dt> <dd>

La classe [**CIM \_ WORMDrive**](cim-wormdrive.md) rappresenta le funzionalità e la gestione di un'unità worm, un sottotipo del dispositivo di accesso multimediale.

</dd> </dl>

 

 
