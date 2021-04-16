---
title: Principali strumenti e tecniche per creare giochi Windows più affidabili
description: Questo articolo descrive gli strumenti e le tecniche che è possibile usare per ridurre il numero di chiamate di supporto ricevute.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76b49c228af6a932c453b11e92f612d3419a4af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473662"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>Principali strumenti e tecniche per creare giochi Windows più affidabili

Uno dei costi più indesiderati che riguardano la produzione di giochi è il supporto delle chiamate. Ogni volta che un utente contatta il supporto tecnico, il profitto del gioco viene ridotto. Sebbene alcune chiamate al supporto tecnico non siano prevenibili, altre possono essere eliminate o ridotte mediante procedure di sviluppo ottimali. Questo articolo descrive gli strumenti e le tecniche che è possibile usare per ridurre il numero di chiamate di supporto ricevute.

Tutti gli strumenti descritti in questo articolo sono gratuiti e le tecniche sono abbastanza semplici da aggiungere alla maggior parte dei metodi di sviluppo.

Strumenti e tecniche:

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Microsoft Application Compatibility Toolkit](#microsoft-application-compatibility-toolkit)
-   [Test di protezione dell'account utente](#user-account-protection-testing)
-   [PIX per Windows](#pix-for-windows)
-   [Rilevamento configurazione](#configuration-detection)
-   [Abilita avvisi del compilatore completi](#enable-full-compiler-warnings)
-   [Server di simboli Microsoft](#microsoft-symbol-server)
-   [Segnalazione errori Windows](#windows-error-reporting)
-   [Strumenti di ottimizzazione delle prestazioni](#performance-tuning-tools)
-   [Summary](#summary)

## <a name="prefast"></a>PREfast

PREfast per i driver è uno strumento offerto da Microsoft che analizza i percorsi di esecuzione in C o C++ compilato per individuare i bug in fase di esecuzione. La funzione PREfast opera attraverso tutti i percorsi di esecuzione in tutte le funzioni e la valutazione di ogni percorso per individuare eventuali problemi. Anche se questo strumento viene in genere usato per sviluppare driver e altro codice kernel, può aiutare gli sviluppatori di giochi a risparmiare tempo eliminando alcuni bug difficili da trovare o ignorati dal compilatore. L'uso di PREfast è un ottimo modo per ridurre il carico di lavoro post-rilascio e i costi di supporto.

PREfast viene fornita con Visual Studio Team System e come parte del [Kit driver di Windows](https://www.microsoft.com/whdc/devtools/WDK/). Per ulteriori informazioni su PREfast, vedere [PREfast per i driver](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

Microsoft Application Verifier, o AppVerifier, è uno strumento che può aiutare i tester fornendo più funzioni in uno strumento. AppVerifier è stato sviluppato per semplificare la verifica degli errori di programmazione comuni. AppVerifier può controllare i parametri passati nelle chiamate API, inserire input errato per verificare la capacità di gestione degli errori e registrare le modifiche al registro di sistema e file system. AppVerifier è anche in grado di rilevare i sovraccarichi del buffer nell'heap, verificare che un elenco di controllo di accesso (ACL) sia stato definito correttamente e imporre l'uso sicuro delle API Sockets.

Anche se non esaustivo, AppVerifier può essere un componente aggiuntivo della casella degli strumenti di un tester per consentire a uno sviluppo studio di rilasciare un prodotto di qualità e ridurre i potenziali costi post-rilascio.

Per ulteriori informazioni su Application Verifier, vedere [Application Verifier](/previous-versions/ms220948(v=vs.80)) e [utilizzo di Application Verifier all'interno del ciclo](/previous-versions/aa480483(v=msdn.10)) di vita di sviluppo del software su MSDN. È possibile scaricare Application Verifier dal [download dei dettagli: Application Verifier](https://www.microsoft.com/download/details.aspx?id=20028) nell'area download Microsoft.

È disponibile anche uno strumento simile per i driver, Driver Verifier. Per ulteriori informazioni, vedere [utilizzo di Driver Verifier per identificare i problemi relativi ai driver di Windows per utenti avanzati](https://support.microsoft.com/Default.aspx?kbid=244617) nel supporto tecnico Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Microsoft Application Compatibility Toolkit

Microsoft Application Compatibility Toolkit è un set di strumenti gratuiti per aiutare gli sviluppatori a verificare rapidamente il modo in cui le loro versioni eseguiranno i nuovi Service Pack rilasciati per Microsoft Windows. Essendo pronti per i nuovi Service Pack, gli sviluppatori possono prevenire o essere pronti per eventuali problemi.

Application Compatibility Toolkit e altre informazioni sono reperibili nella pagina relativa alla [compatibilità delle applicazioni Windows](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx).

## <a name="user-account-protection-testing"></a>Test di protezione dell'account utente

Windows Vista e Windows 7 hanno due tipi principali di account utente: utente standard e amministratore. Gli account utente standard sono il tipo preferito per tutti gli utenti, in quanto riducono il rischio di danneggiamento del sistema da parte di applicazioni dannose. Poiché l'utente standard ha restrizioni di accesso, ad esempio non è in grado di scrivere nella cartella programmi o \_ \_ nel computer locale HKEY (HKLM) nel registro di sistema, è importante che i giochi siano progettati e testati per funzionare con un account utente standard.

Per ulteriori informazioni su questo argomento, vedere l'articolo relativo alla [patch del software di gioco in Windows XP, Windows Vista e Windows 7](./patching-methods-in-windows-xp-and-vista.md) e [controllo dell'account utente per gli sviluppatori di giochi](./user-account-control-for-game-developers.md).

## <a name="pix-for-windows"></a>PIX per Windows

PIX è uno strumento per la raccolta e l'analisi delle informazioni sulle prestazioni da un'applicazione in esecuzione. PIX è in grado di raccogliere dati statistici sul motivo per cui alcuni frame eseguono il rendering più lentamente rispetto ad altri e possono identificare un utilizzo dell'API scadente PIX può inoltre essere automatizzato per testare la compilazione giornaliera e contrassegnare modifiche improvvise nelle prestazioni dell'applicazione. Utilizzando PIX in un'ampia gamma di configurazioni hardware, i tester e gli sviluppatori possono contribuire a ridurre al minimo le chiamate di supporto correlate alle prestazioni dei giochi.

## <a name="configuration-detection"></a>Rilevamento configurazione

Le funzionalità del dispositivo esposte dai driver non sono sempre corrette. Una soluzione consiste nell'usare un sistema basato su database per la configurazione delle applicazioni, come il sistema illustrato nell'esempio ConfigSystem, incluso in DirectX SDK. Un modello di rilevamento simile al sistema nell'esempio consente di identificare le funzionalità del dispositivo che ostacolano le prestazioni dei giochi e quindi di ridurre il numero di chiamate di supporto sulle prestazioni.

## <a name="enable-full-compiler-warnings"></a>Abilita avvisi del compilatore completi

È consigliabile ripristinare eventuali avvisi del compilatore disabilitati da **\# pragma warning** quando un progetto diventa stabile. Gli sviluppatori devono tentare di eliminare tutti gli avvisi prima di rilasciare un prodotto. Anche se un avviso non causa un arresto anomalo o un errore nel sistema di uno sviluppatore, potrebbe comunque causare un problema sul sistema di un utente. Se non è possibile eliminare un avviso, il team di test deve verificare se l'avviso provocherà pochi o nessun errore nel sistema dell'utente.

## <a name="microsoft-symbol-server"></a>Server di simboli Microsoft

Microsoft fornisce un server accessibile da Internet che fornisce i file di simboli per i sistemi operativi Microsoft Windows, oltre ad altri prodotti Microsoft. I simboli sono inoltre disponibili dal server per le versioni beta correnti e i candidati di rilascio dei prodotti Windows, oltre a correzioni rapide e Service Pack. È possibile configurare il debugger per scaricare i simboli in base alle esigenze durante una sessione di debug, anziché scaricare i file di simboli separatamente prima di una sessione di debug. I simboli vengono scaricati in un percorso di directory specificato dall'utente e vengono caricati dal debugger.

Per ulteriori informazioni sul server dei simboli Microsoft, vedere [strumenti e simboli di debug: introduzione](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Segnalazione errori Windows

Segnalazione errori Windows (WER) è un servizio fornito da Microsoft per aiutare gli sviluppatori a raccogliere informazioni sugli errori dalle applicazioni in modo unificato e organizzato. Sebbene sia completamente volontario, gli sviluppatori dovrebbero sfruttare questo servizio per determinare quali bug si verificano più spesso. L'uso di WER può essere utile per il debug di problemi comunemente segnalati, che consente di eliminare le chiamate di supporto per i bug più comuni.

Per altre informazioni su WER, vedere [analisi dei dump di arresto anomalo](./crash-dump-analysis.md)del sistema.

## <a name="performance-tuning-tools"></a>Strumenti di ottimizzazione delle prestazioni

Gli sviluppatori possono usare gli analizzatori di prestazioni per ottimizzare le prestazioni del proprio gioco. Oltre a PIX, sono disponibili numerosi analizzatori delle prestazioni per Windows, ad esempio [Intel VTune Performance Analyzer](https://software.intel.com/intel-vtune/) e [AMD codeanalystt Performance Analyzer](https://developer.amd.com/cpu/CodeAnalyst/). Questi strumenti consentono di identificare i colli di bottiglia e di decidere come migliorare le prestazioni complessive di un'applicazione. Il miglioramento dei colli di bottiglia delle prestazioni prima del rilascio consentirà di ridurre i costi post-rilascio.

## <a name="summary"></a>Riepilogo

Tutti gli utenti interessati a progettazione, sviluppo e test devono prendere in considerazione il modo in cui il suo lavoro influirà sul costo post-rilascio di un prodotto. Utilizzando gli strumenti e i metodi indicati in un processo di produzione, è possibile ridurre il volume delle chiamate al supporto. Questo, a sua volta, aumenta i profitti riducendo i costi post-rilascio dello sviluppo di giochi.

 

 