---
description: COM+ versione 1.5 aggiunge nuove funzionalità progettate per aumentare la scalabilità, la disponibilità e la gestibilità complessive delle applicazioni COM+ sia per gli sviluppatori che per gli amministratori di sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novità di COM+ 1.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304882"
---
# <a name="whats-new-in-com-15"></a>Novità di COM+ 1.5

COM+ versione 1.5 aggiunge nuove funzionalità progettate per aumentare la scalabilità, la disponibilità e la gestibilità complessive delle applicazioni COM+ sia per gli sviluppatori che per gli amministratori di sistema.

COM+ 1.5 è disponibile a partire da Windows XP e Windows Server 2003. Le nuove funzionalità di COM+ 1.5 non sono disponibili in Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level di accesso abilitati per impostazione predefinita

Come parte della sicurezza avanzata del sistema, i controlli di accesso sono abilitati per impostazione predefinita quando si crea un'applicazione COM+. Nelle versioni precedenti i controlli di accesso sono stati disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente. A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente. Per altre informazioni e procedure su come modificare [](enabling-access-checks-at-the-component-level.md) le impostazioni [predefinite,](enabling-access-checks-for-an-application.md)vedere Creazione di una nuova applicazione [COM+,](creating-a-new-com--application.md)abilitazione dei controlli di accesso per un'applicazione e abilitazione dei controlli di accesso a livello di componente.

## <a name="application-pooling"></a>Pool di applicazioni

Con la nuova proprietà ConcurrentApps dell'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) nella raccolta [**Applications,**](applications.md) il pool di applicazioni COM+ aggiunge scalabilità per i processi a thread singolo e si integra con il nuovo servizio Riciclo applicazioni COM+. Per [informazioni dettagliate,](com--application-pooling.md) vedere Pool di applicazioni COM+.

## <a name="application-recycling"></a>Riciclo delle applicazioni

Il riciclo delle applicazioni aumenta significativamente la stabilità complessiva delle applicazioni. Poiché le prestazioni della maggior parte delle applicazioni possono peggiorare nel tempo a causa di fattori quali perdite di memoria, affidamento sul codice di terze parti e utilizzo non scalabile delle risorse, il riciclo delle applicazioni COM+ offre una soluzione semplice per arrestare correttamente un processo associato a un'applicazione e riavviarlo. Per [informazioni dettagliate, vedere Riciclo](com--application-recycling.md) delle applicazioni COM+. Vedere anche "Configurazione del riciclo dei processi" nella Guida dell'amministrazione di Servizi componenti per una procedura dettagliata per la configurazione del riciclo dei processi.

## <a name="com-partitions"></a>Partizioni COM+

In questa versione COM+ introduce il supporto per le partizioni COM+, una funzionalità che consente l'installazione e la configurazione di più versioni di applicazioni COM+ nello stesso computer. Questa funzionalità consente di risparmiare sui costi e sull'utilizzo di più server per gestire versioni diverse di un'applicazione. In un singolo computer, ogni partizione agisce, in effetti, come server virtuale. Dopo aver installato l'applicazione in ogni partizione, creare set di partizioni che eseercitino il mapping degli utenti ai server logici. Per [informazioni dettagliate su come](com--partitions.md) configurare e gestire le partizioni COM+, vedere Partizioni COM+. Per le procedure dettagliate, vedere anche "Amministrazione delle partizioni applicazioni" nella Guida per l'amministrazione di Servizi componenti.

## <a name="com-services-without-components"></a>Servizi COM+ senza componenti

Con COM+ 1.5 è possibile usare i servizi forniti da COM+ senza dover compilare un componente per contenere i metodi che chiamano tali servizi. Ciò è molto vantaggioso per gli sviluppatori che in genere non usano componenti, ma vogliono usare i servizi COM+, ad esempio le transazioni o il tracker COM+. Usando i servizi COM+ senza componenti, gli sviluppatori possono evitare il sovraccarico della creazione di un componente usato per accedere solo ai servizi COM+ necessari. Per [informazioni dettagliate, vedere Servizi COM+](com--services-without-components.md) senza componenti.

## <a name="com-soap-service"></a>Servizio SOAP COM+

Con COM+ 1.5 è ora possibile esporre un'applicazione COM+ come servizio Web XML. È anche possibile usare in modo trasparente un servizio Web XML, indipendentemente dal fatto che sia distribuito con COM+ o meno, come componente COM. Ciò significa che è possibile creare facilmente nuovi servizi Web XML da applicazioni COM+ esistenti e incorporare facilmente servizi Web XML in nuove applicazioni COM+. Per [informazioni dettagliate, vedere](com--soap-service.md) Servizio SOAP COM+.

## <a name="configurable-isolation-levels"></a>Livelli di isolamento configurabili

Gli sviluppatori COM+ possono usare la nuova proprietà TxIsolationLevel o lo strumento amministrativo Servizi componenti per configurare il livello di isolamento di un'applicazione in base alle necessità, consentendo di aumentare la concorrenza, le prestazioni e la scalabilità. Questa flessibilità consente a chi ha la giusta competenza di ottenere ogni ultima oncia di velocità effettiva dalle applicazioni. Per [informazioni dettagliate, vedere Configurazione dei livelli](configuring-transaction-isolation-levels.md) di isolamento delle transazioni.

## <a name="creating-private-components"></a>Creazione di componenti privati

Negli scenari in cui in un'applicazione sono presenti diversi componenti helper che devono essere chiamati solo da altri componenti all'interno di tale applicazione, questa versione di COM+ consente di usare una nuova proprietà, IsPrivateComponent, per contrassegnare questi componenti come privati. Nella versione precedente di COM+, tutti i componenti dovevano essere pubblici per poter accedere ai servizi COM+, il che significa che questi componenti potevano essere attivati da altre applicazioni. Un componente privato può essere visualizzato e attivato solo da altri componenti nella stessa applicazione, offrendo un maggiore controllo sulle funzionalità da esporre. È necessario documentare e gestire solo i componenti pubblici, mentre si usano componenti privati a cui non è possibile accedere dall'esterno dell'applicazione, ma che possono comunque sfruttare tutti i servizi COM+.

## <a name="dtc-security-settings"></a>Sicurezza DTC Impostazioni

Sono state aggiunte diverse nuove impostazioni di sicurezza per il Microsoft Distributed Transaction Coordinator (DTC), che consentono di personalizzare i livelli di sicurezza per la gestione delle transazioni distribuite. Vedere Considerazioni sulla sicurezza DTC su queste impostazioni e su come implementarle.

Per facilitare l'autenticazione reciproca, il DTC è limitato all'esecuzione con l'account NetworkService. Per informazioni dettagliate, vedere Gestione di account e privilegi.

Per il ripristino con i database XA, è consigliabile che all'account NetworkService siano fornite le autorizzazioni e i ruoli necessari per eseguire il ripristino. Il metodo esatto per eseguire questa operazione è specifico per ogni database. Per altre informazioni, vedere Disabilitazione di transazioni distribuite native e Disabilitazione delle transazioni TIP e XA.

Per offrire un sistema più sicuro quando si usano transazioni XA, le piattaforme Windows Server 2003 includono una nuova voce del Registro di sistema per specificare i file DLL XA. Quando si esegue l'aggiornamento a Windows Server 2003, è possibile usare le transazioni XA come prima creando una voce del Registro di sistema in **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ MSDTC \\ XADLL**, dove il nome del valore è il nome della DLL (nel formato *dllname*.dll) e il valore è il percorso completo del file DLL. È necessario creare una voce per ogni file DLL XA in uso. Se il computer che esegue DTC fa parte di un cluster, è necessario creare la voce del Registro di sistema per ogni nodo del cluster. Per altre informazioni, vedere Gestione delle transazioni XA.

## <a name="low-memory-activation-gates"></a>Low-Memory di attivazione

Con questa versione, COM+ controlla automaticamente la memoria prima di creare un server o un oggetto COM+. Se la percentuale di memoria virtuale disponibile per l'applicazione scende al di sotto di una soglia fissa, l'attivazione non riesce prima della creazione dell'oggetto. In caso contrario, queste attivazioni che normalmente verrebbero eseguite, il servizio Porte di [Low-Memory COM+](com--low-memory-activation-gates.md) migliora notevolmente l'affidabilità del sistema.

## <a name="moving-and-copying-com-components"></a>Spostamento e copia di componenti COM

Con questa versione, COM+ consente di spostare e copiare i componenti. Ciò significa che è possibile configurare una singola implementazione fisica di un componente più volte. Si ottiene il riutilizzo dei componenti a livello binario anziché a livello di codice sorgente, con una riduzione del codice, costi di sviluppo inferiori e tempi di commercializzazione più rapidi. Per [informazioni dettagliate,](moving-components.md) vedere [Spostamento di componenti](copying-components.md) e copia dei componenti.

## <a name="network-access"></a>Accesso alla rete

L'accesso alla rete COM+ è disabilitato per impostazione predefinita Windows Server 2003, ovvero COM+ può essere usato solo in locale per impostazione predefinita. Usare la procedura seguente per abilitare l'accesso COM+ di rete.

**Per abilitare l'accesso COM+ di rete**

1.  Scegliere Installazione **applicazioni** dal menu **Start Pannello di controllo** quindi selezionare **Installazione applicazioni**.

2.  Fare **clic su Aggiungi/Rimuovi Windows componenti**.

3.  Selezionare **Server applicazioni** e fare clic su **Dettagli**.

4.  Selezionare la casella accanto a **Abilita accesso COM+ di** rete e quindi fare clic su **OK.**

5.  Fare **clic su** Avanti per completare la procedura guidata Windows componenti.

6.  Fare **clic su** Fine per chiudere la procedura guidata.

L'accesso alle transazioni di rete DTC è disabilitato per impostazione predefinita Windows Server 2003. In queste piattaforme, DTC può eseguire solo transazioni locali per impostazione predefinita. Usare la procedura seguente per abilitare l'accesso DTC di rete.

> [!NOTE]
> È anche possibile abilitare l'accesso DTC di rete usando lo strumento amministrativo Servizi componenti o a livello di codice tramite la libreria di amministrazione COM+. Per informazioni procedurali, vedere "Configurazione della sicurezza DTC" nella Guida dell'amministrazione di Servizi componenti.

**Per abilitare l'accesso DTC di rete**

1.  Scegliere Installazione **applicazioni** dal menu **Start Pannello di controllo** quindi selezionare **Installazione applicazioni**.

2.  Fare **clic su Aggiungi/Rimuovi Windows componenti**.

3.  Selezionare **Server applicazioni** e fare clic su **Dettagli**.

4.  Selezionare la casella accanto a **Abilita accesso DTC di** rete e quindi fare clic su **OK.**

5.  Fare **clic su** Avanti per completare la procedura guidata Windows componenti.

6.  Fare **clic su** Fine per chiudere la procedura guidata.

## <a name="pausing-and-disabling-applications"></a>Sospensione e disabilitazione delle applicazioni

Le applicazioni COM+ sono ora più gestibili. Un amministratore può sospendere e riprendere le applicazioni server COM+, disabilitare e abilitare le applicazioni server o la libreria COM+ o anche singoli componenti configurati. Entrambe le funzionalità di sospensione e disabilitazione impediscono le attivazioni future senza influire sulle istanze del componente esistenti. Per altre informazioni, vedere "Amministrazione di applicazioni COM+" nella Guida dell'amministrazione di Servizi componenti.

## <a name="process-dumping"></a>Dump dei processi

Non è facile risolvere i problemi delle applicazioni in un ambiente di produzione. Come si raccolgono informazioni su un problema senza disturbare i processi in esecuzione? COM+ offre ora una soluzione tramite la nuova funzionalità di dump del processo. Questa funzionalità consente all'amministratore di sistema di eseguire il dump dell'intero stato di un processo senza terminarlo. Per altre informazioni, vedere "Amministrazione dello strumento di dump dei processi per il debug di applicazioni COM+" nella Guida dell'amministrazione di Servizi componenti.

## <a name="process-initialization"></a>Inizializzazione del processo

Molte applicazioni server devono eseguire operazioni di inizializzazione e pulizia specifiche quando vengono avviate e arrestate. Quando si esegue Windows Server 2003, è possibile creare una classe che implementa [**l'interfaccia IProcessInitializer.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) All'avvio del processo, chiama [**IProcessInitializer::Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) e all'arresto chiama [**IProcessInitializer::Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). In questo modo il componente può eseguire le attività necessarie, ad esempio l'inizializzazione di connessioni, file e cache.

## <a name="running-com-applications-as-nt-services"></a>Esecuzione di applicazioni COM+ come servizi NT

Gli sviluppatori COM+ possono ora usare lo strumento amministrativo Servizi componenti per configurare e implementare un'applicazione server COM+ come servizio NT. Ciò significa che il server può essere avviato o riavviato automaticamente se l'applicazione deve sempre essere in esecuzione. che l'applicazione COM+ possa essere eseguita come account di sistema locale se deve eseguire operazioni con privilegi; e che i servizi dipendenti dell'applicazione possono ora essere avviati automaticamente. Per [informazioni dettagliate, vedere](com--applications-running-as-service-applications.md) Applicazioni COM+ in esecuzione come applicazioni di servizio.

## <a name="side-by-side-assemblies"></a>Assembly side-by-side

Gli assembly side-by-side (SxS) consentono alle applicazioni di specificare la versione di una DLL di sistema o di un componente COM classico da usare, ad esempio MDAC, MFS, MSVCRT o MSXML. Ad esempio, se un'applicazione ASP si basa su MSXML versione 2.0, è possibile assicurarsi che questa applicazione usi ancora MSXML versione 2.0 anche dopo l'applicazione dei Service Pack al server. Ciò significa che, anche quando nel computer MSXML una nuova versione di , la versione 2.0 rimane e viene usata dall'applicazione.

Per configurare gli assembly SxS, è necessario conoscere il percorso della DLL e che il file manifesto COM+ esista in ogni directory virtuale che deve usare la DLL. Il manifesto COM+ è un file XML che contiene informazioni sulla posizione in cui è installata una DLL. Il manifesto viene usato per creare un contesto di attivazione per l'applicazione. I contesti di attivazione consentono a un'applicazione di caricare una determinata versione della DLL, un'istanza dell'oggetto COM o una versione di finestra personalizzata. È possibile usare lo strumento amministrativo Servizi componenti o la proprietà ApplicationDirectory per immettere il percorso completo della directory radice dell'applicazione che contiene un file manifesto dell'assembly SxS valido. Per altre informazioni, vedere Applicazioni isolate e assembly [side-by-side](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Segnalazione errori Windows

COM+ 1.5 include il supporto per il componente Segnalazione errori Windows (WER), disponibile a partire da Windows XP. WeR consente agli utenti di notificare a Microsoft errori dell'applicazione, errori del kernel e applicazioni che non rispondono. Queste notifiche consentono ai team di supporto tecnico Microsoft di risolvere i problemi tecnici in modo più efficace. Inoltre, il componente Segnalazione errori Windows consente agli sviluppatori COM+ di ricevere informazioni che possono essere usate per migliorare le applicazioni. Per altre informazioni, vedere [Segnalazione errori Windows](/windows/desktop/wer/windows-error-reporting).

 

 
