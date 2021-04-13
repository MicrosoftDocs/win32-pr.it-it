---
description: COM+ versione 1,5 aggiunge nuove funzionalità progettate per aumentare la scalabilità, la disponibilità e la gestibilità delle applicazioni COM+ sia per gli sviluppatori che per gli amministratori di sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novità di COM+ 1,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994237002ea5d19c2cb00364f1064df38ed7271f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401484"
---
# <a name="whats-new-in-com-15"></a>Novità di COM+ 1,5

COM+ versione 1,5 aggiunge nuove funzionalità progettate per aumentare la scalabilità, la disponibilità e la gestibilità delle applicazioni COM+ sia per gli sviluppatori che per gli amministratori di sistema.

COM+ 1,5 è disponibile a partire da Windows XP e Windows Server 2003. Le nuove funzionalità COM+ 1,5 non sono disponibili in Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Controlli di accesso Application-Level abilitati per impostazione predefinita

Nell'ambito della sicurezza avanzata del sistema, i controlli di accesso vengono abilitati per impostazione predefinita durante la creazione di un'applicazione COM+. Nelle versioni precedenti, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente. A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente. Vedere [creazione di una nuova applicazione com+](creating-a-new-com--application.md), [Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)e [Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md) per ulteriori informazioni e procedure su come modificare le impostazioni predefinite.

## <a name="application-pooling"></a>Pool di applicazioni

Con la nuova proprietà ConcurrentApps dell'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) nella raccolta di [**applicazioni**](applications.md) , il pool di applicazioni com+ aggiunge la scalabilità per i processi a thread singolo e si integra con il nuovo servizio di riciclo delle applicazioni com+. Per informazioni dettagliate, vedere [pool di applicazioni com+](com--application-pooling.md) .

## <a name="application-recycling"></a>Riciclo delle applicazioni

Il riciclo delle applicazioni aumenta significativamente la stabilità complessiva delle applicazioni. Poiché le prestazioni della maggior parte delle applicazioni possono peggiorare nel tempo a causa di fattori quali le perdite di memoria, la dipendenza dal codice di terze parti e l'utilizzo non scalabile delle risorse, il riciclo delle applicazioni COM+ fornisce una soluzione semplice per arrestare normalmente un processo associato a un'applicazione e riavviarlo. Per informazioni dettagliate, vedere [riciclo delle applicazioni com+](com--application-recycling.md) . Vedere anche "configurazione del riciclo dei processi" nella Guida di amministrazione di Servizi componenti per una procedura dettagliata per la configurazione del riciclo dei processi.

## <a name="com-partitions"></a>Partizioni COM+

In questa versione, COM+ introduce il supporto per le partizioni COM+, una funzionalità che consente l'installazione e la configurazione di più versioni di applicazioni COM+ nello stesso computer. Questa funzionalità consente di risparmiare sul costo e sul tempo richiesto per l'utilizzo di più server per la gestione di versioni diverse di un'applicazione. In un singolo computer, ogni partizione agisce in effetti come server virtuale. Dopo aver installato l'applicazione in ogni partizione, è possibile creare set di partizioni che esegue il mapping degli utenti ai server logici. Per informazioni dettagliate su come configurare e gestire le partizioni COM+, vedere [partizioni com+](com--partitions.md) . Vedere anche "amministrazione delle partizioni dell'applicazione" nella Guida dell'amministrazione di Servizi componenti per le procedure dettagliate.

## <a name="com-services-without-components"></a>Servizi COM+ senza componenti

Con COM+ 1,5, è possibile utilizzare i servizi forniti da COM+ senza che sia necessario compilare un componente che contenga i metodi che chiamano tali servizi. Si tratta di un vantaggio molto vantaggioso per gli sviluppatori che in genere non utilizzano componenti, ma che desiderano utilizzare servizi COM+ quali transazioni o lo strumento di rilevamento COM+. Utilizzando i servizi COM+ senza componenti, gli sviluppatori possono evitare il sovraccarico dovuto alla creazione di un componente utilizzato per accedere solo ai servizi COM+ necessari. Per informazioni dettagliate, vedere [com+ Services without Components](com--services-without-components.md) .

## <a name="com-soap-service"></a>Servizio SOAP COM+

Con COM+ 1,5, è ora possibile esporre un'applicazione COM+ come un servizio Web XML. È inoltre possibile utilizzare in modo trasparente un servizio Web XML, indipendentemente dal fatto che sia distribuito utilizzando COM+ o meno, come componente COM. Ciò significa che è possibile creare facilmente nuovi servizi Web XML dalle applicazioni COM+ esistenti e incorporare facilmente i servizi Web XML in nuove applicazioni COM+. Per informazioni dettagliate, vedere [servizio SOAP com+](com--soap-service.md) .

## <a name="configurable-isolation-levels"></a>Livelli di isolamento configurabili

Gli sviluppatori COM+ possono utilizzare la nuova proprietà proprietà TxIsolationLevel o lo strumento di amministrazione Servizi componenti per configurare il livello di isolamento di un'applicazione in base alle esigenze, contribuendo ad aumentare la concorrenza, le prestazioni e la scalabilità. Questa flessibilità consente agli utenti con la giusta quantità di competenze di ottenere tutte le ultime once di velocità effettiva delle applicazioni. Per informazioni dettagliate, vedere [configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md) .

## <a name="creating-private-components"></a>Creazione di componenti privati

Negli scenari in cui sono presenti diversi componenti helper in un'applicazione che devono essere chiamati solo da altri componenti all'interno di tale applicazione, questa versione di COM+ consente di utilizzare una nuova proprietà, IsPrivateComponent, per contrassegnare questi componenti come privati. Nella versione precedente di COM+ tutti i componenti di devono essere pubblici per poter accedere ai servizi COM+, il che significa che questi componenti potrebbero essere attivati da altre applicazioni. Un componente privato può essere visualizzato e attivato solo da altri componenti nella stessa applicazione, garantendo un maggiore controllo sulle funzionalità da esporre. È necessario solo documentare e gestire i componenti pubblici, mentre si usano componenti privati a cui non è possibile accedere dall'esterno dell'applicazione, ma che possono comunque sfruttare tutti i servizi COM+.

## <a name="dtc-security-settings"></a>Impostazioni di sicurezza di DTC

Per Microsoft Distributed Transaction Coordinator (DTC) sono state aggiunte alcune nuove impostazioni di sicurezza che consentono di personalizzare i livelli di sicurezza per la gestione delle transazioni distribuite. Vedere Considerazioni sulla sicurezza di DTC su queste impostazioni e su come implementarle.

Per semplificare l'autenticazione reciproca, DTC è limitato all'esecuzione con l'account NetworkService. Per informazioni dettagliate, vedere Gestione di account e privilegi.

Per il ripristino con i database XA, è consigliabile specificare le autorizzazioni e i ruoli necessari per eseguire il ripristino per l'account NetworkService. Il metodo esatto per eseguire questa operazione è specifico per ogni database. Per ulteriori informazioni, vedere disabilitare le transazioni distribuite native e disabilitare le transazioni TIP e XA.

Per fornire un sistema più sicuro quando si usano le transazioni XA, le piattaforme Windows Server 2003 includono una nuova voce del registro di sistema per specificare i file DLL XA. Quando si esegue l'aggiornamento a Windows Server 2003, è possibile utilizzare le transazioni XA come prima creando una voce del registro di sistema in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MSDTC \\ XADLL**, dove il nome del valore è il nome della dll (nel formato *dllname*. dll) e il valore è il percorso completo del file dll. È necessario creare una voce per ogni file DLL XA in uso. Se il computer che esegue DTC fa parte di un cluster, è necessario effettuare la voce del registro di sistema per ogni nodo del cluster. Per ulteriori informazioni, vedere Managing XA Transactions.

## <a name="low-memory-activation-gates"></a>Controlli di attivazione Low-Memory

Con questa versione, COM+ controlla automaticamente la memoria prima di creare un oggetto o un server COM+. Se la percentuale di memoria virtuale disponibile per l'applicazione scende al di sotto di una soglia fissa, l'attivazione avrà esito negativo prima della creazione dell'oggetto. Se queste attivazioni non vengono eseguite correttamente, il servizio [COM+ Low-Memory Activation Gates](com--low-memory-activation-gates.md) migliora significativamente l'affidabilità del sistema.

## <a name="moving-and-copying-com-components"></a>Trasferimento e copia di componenti COM

Con questa versione, COM+ consente di spostare e copiare i componenti. Ciò significa che è possibile configurare una singola implementazione fisica di un componente in tempi diversi. Si ottiene il riutilizzo dei componenti a livello binario piuttosto che a livello di codice sorgente, il che comporta un minor numero di codice, costi di sviluppo inferiori e tempi di immissione sul mercato più rapidi. Per informazioni dettagliate, vedere [movimento di componenti](moving-components.md) e [copia di componenti](copying-components.md) .

## <a name="network-access"></a>Accesso alla rete

L'accesso alla rete COM+ è disabilitato per impostazione predefinita in Windows Server 2003, pertanto è possibile utilizzare COM+ solo localmente per impostazione predefinita. Utilizzare la procedura seguente per abilitare l'accesso COM+ alla rete.

**Per abilitare l'accesso COM+ alla rete**

1.  Dal menu **Start** scegliere **Pannello di controllo** e quindi **Installazione applicazioni**.

2.  Fare clic su **Aggiungi/Rimuovi componenti di Windows**.

3.  Selezionare **Server applicazioni** e fare clic su **Dettagli**.

4.  Selezionare la casella accanto a **Abilita accesso com+ alla rete**, quindi fare clic su **OK**.

5.  Fare clic su **Avanti** per completare la procedura guidata componenti di Windows.

6.  Fare clic su **fine** per chiudere la procedura guidata.

L'accesso alle transazioni di rete DTC è disabilitato per impostazione predefinita in Windows Server 2003. In queste piattaforme, DTC può eseguire solo transazioni locali per impostazione predefinita. Utilizzare la procedura seguente per abilitare l'accesso DTC alla rete.

> [!NOTE]
> È inoltre possibile abilitare l'accesso DTC alla rete utilizzando lo strumento di amministrazione Servizi componenti o a livello di codice tramite la libreria di amministrazione COM+. Per informazioni sulle procedure, vedere la sezione relativa alla configurazione della sicurezza di DTC nella Guida all'amministrazione di Servizi componenti.

**Per abilitare l'accesso DTC alla rete**

1.  Dal menu **Start** scegliere **Pannello di controllo** e quindi **Installazione applicazioni**.

2.  Fare clic su **Aggiungi/Rimuovi componenti di Windows**.

3.  Selezionare **Server applicazioni** e fare clic su **Dettagli**.

4.  Selezionare la casella accanto a **Abilita accesso DTC alla rete**, quindi fare clic su **OK**.

5.  Fare clic su **Avanti** per completare la procedura guidata componenti di Windows.

6.  Fare clic su **fine** per chiudere la procedura guidata.

## <a name="pausing-and-disabling-applications"></a>Sospensione e disabilitazione delle applicazioni

Le applicazioni COM+ sono ora più gestibili. Un amministratore può sospendere e riprendere le applicazioni server COM+ o disabilitare e abilitare la libreria COM+ o le applicazioni server o anche singoli componenti configurati. Entrambe le funzionalità di sospensione e disabilitazione impediscono le attivazioni future senza influire sulle istanze dei componenti esistenti. Per ulteriori informazioni, vedere "amministrazione delle applicazioni COM+" nella Guida all'amministrazione di Servizi componenti.

## <a name="process-dumping"></a>Dump del processo

Non è facile risolvere i problemi delle applicazioni in un ambiente di produzione. In che modo è possibile raccogliere informazioni su un problema senza compromettere i processi in esecuzione? COM+ ora fornisce una soluzione tramite la nuova funzionalità di dump del processo. Questa funzionalità consente all'amministratore di sistema di eseguire il dump dell'intero stato di un processo senza terminarlo. Per ulteriori informazioni, vedere l'argomento relativo alla gestione dello strumento di dump del processo per il debug delle applicazioni COM+ nella Guida di amministrazione di Servizi componenti.

## <a name="process-initialization"></a>Inizializzazione processo

In molte applicazioni server è necessario eseguire operazioni di inizializzazione e pulizia specifiche quando vengono avviate e arrestate. Quando è in esecuzione in Windows Server 2003, è possibile creare una classe che implementi l'interfaccia [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) . All'avvio del processo, viene chiamato [**IProcessInitializer:: Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) e, al momento dell'arresto, viene chiamato [**IProcessInitializer:: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Questo consente al componente di eseguire le attività necessarie, ad esempio l'inizializzazione di connessioni, file e cache.

## <a name="running-com-applications-as-nt-services"></a>Esecuzione di applicazioni COM+ come servizi NT

Gli sviluppatori COM+ possono ora utilizzare lo strumento di amministrazione Servizi componenti per configurare e implementare un'applicazione server COM+ come servizio NT. Ciò significa che il server può essere avviato o riavviato automaticamente se l'applicazione deve essere sempre in esecuzione. che l'applicazione COM+ possa essere eseguita come account di sistema locale se è necessario eseguire operazioni privilegiate. e che i servizi dipendenti dell'applicazione possono ora essere avviati automaticamente. Per informazioni dettagliate, vedere [applicazioni com+ in esecuzione come applicazioni di servizio](com--applications-running-as-service-applications.md) .

## <a name="side-by-side-assemblies"></a>Assembly affiancati

Gli assembly side-by-Side (SxS) consentono alle applicazioni di specificare quale versione di una DLL di sistema o di un componente COM classico usare, ad esempio MDAC, MFS, MSVCRT o MSXML. Se, ad esempio, un'applicazione ASP si basa su MSXML versione 2,0, è possibile verificare che l'applicazione usi ancora MSXML versione 2,0 anche dopo l'applicazione dei Service Pack al server. Ovvero, anche quando viene installata una nuova versione di MSXML nel computer, la versione 2,0 rimane e viene usata dall'applicazione.

Per configurare gli assembly SxS, è necessario individuare il percorso della DLL e il file manifesto COM+ presente in ogni directory virtuale che deve usare la DLL. Il manifesto COM+ è un file XML che contiene informazioni sulla posizione in cui è installata una DLL. Il manifesto viene utilizzato per creare un contesto di attivazione per l'applicazione. I contesti di attivazione consentono a un'applicazione di caricare una versione specifica della DLL, un'istanza dell'oggetto COM o una versione della finestra personalizzata. È possibile utilizzare lo strumento di amministrazione Servizi componenti o la proprietà ApplicationDirectory per immettere il percorso completo della directory radice dell'applicazione che contiene un file manifesto dell'assembly SxS valido. Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Segnalazione errori Windows

COM+ 1,5 include il supporto per il componente Segnalazione errori Windows (WER), disponibile a partire da Windows XP. WER consente agli utenti di notificare a Microsoft gli errori dell'applicazione, gli errori del kernel e le applicazioni che non rispondono. Queste notifiche consentono ai team di supporto clienti Microsoft di risolvere i problemi tecnici in modo più efficace. Inoltre, il componente Segnalazione errori Windows consente agli sviluppatori COM+ di ricevere informazioni che possono essere utilizzate per migliorare le proprie applicazioni. Per altre informazioni, vedere [Segnalazione errori Windows](/windows/desktop/wer/windows-error-reporting).

 

 
