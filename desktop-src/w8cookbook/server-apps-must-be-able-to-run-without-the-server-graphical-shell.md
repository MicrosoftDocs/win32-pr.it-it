---
title: Restrizioni della shell grafica server
description: Le app Server devono poter essere eseguite senza la shell grafica server
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7666ae07a28d798a36d249bf37ab2d7719b9fba0
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104399866"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Le app Server devono poter essere eseguite senza la shell grafica server

## <a name="platform"></a>Piattaforma

**Server** : Windows Server 2012 

## <a name="description"></a>Descrizione

Shell grafica server, la funzionalità che include Esplora risorse e Internet Explorer, viene installata per impostazione predefinita nelle installazioni "server con GUI" di Windows Server 2012. La funzionalità shell grafica server può essere disinstallata per ridurre il potenziale impatto sulle prestazioni e la manutenzione, limitando in tal modo il numero di riavvii che il server può subire, pur continuando a consentire l'esecuzione locale degli strumenti di gestione nel server.

Dopo che un amministratore ha disinstallato la shell grafica server, il server si trova nella configurazione dell'interfaccia server minima:

![Configurazione interfaccia shell grafica server](images/minimalserverinterface.png)

Gli amministratori possono quindi scegliere di eseguire la configurazione dell'interfaccia server minima (che include un set di strumenti di gestione locali) come impostazione predefinita, anziché nel server con una configurazione GUI. Ciò consente il monitoraggio e la gestione locali, riducendo al tempo stesso l'utilizzo delle risorse e la frequenza di manutenzione.

Gli amministratori possono reinstallare la shell grafica server in un secondo momento se hanno bisogno della funzionalità al suo interno. Gli amministratori possono anche iniziare da un'installazione dei componenti di base del server e "compilare" nella configurazione dell'interfaccia server minima usando le funzionalità su richiesta.

Le applicazioni server devono essere in grado di essere eseguite nella configurazione dell'interfaccia server minima per sfruttare i vantaggi dell'utilizzo ridotto delle risorse e del footprint di manutenzione. Questa funzionalità può essere eseguita consentendo all'amministratore di scegliere di non installare parti dell'app che necessitano della shell grafica server o di rilevare la presenza della shell grafica server e disabilitare alcuni aspetti dell'app.

L'interfaccia server minima presenta una riduzione delle risorse e un footprint di manutenzione perché molte API e file binari inclusi nella shell grafica server non sono disponibili in questa configurazione. Laddove appropriato, le app Server devono anche consentire l'amministrazione remota (preferibilmente tramite la comunicazione remota di Windows PowerShell) da un'altra installazione di Windows Server o client Windows. Ciò consente una migliore amministrazione centralizzata di uno o più computer nella configurazione dell'interfaccia server minima o di computer in una configurazione di footprint ancora inferiore, ad esempio Server Core.

## <a name="manifestation"></a>Manifestazione

Se un'app richiede una delle API o dei file binari che non sono disponibili nella configurazione dell'interfaccia server minima, è possibile che non vengano visualizzati correttamente sullo schermo e/o non siano utilizzabili.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli sviluppatori di app Server devono identificare le parti delle app che richiedono le API o i file binari rimossi e includono le informazioni per l'amministratore del server che identificano le parti dell'app che non vengono eseguite correttamente quando si usa l'interfaccia server minima. Se le parti dell'app possono essere installate facoltativamente o non sono assolutamente necessarie per la funzionalità del prodotto, l'app può comunque essere installata ed eseguita con la configurazione dell'interfaccia server minima.

Se non è possibile usare l'app senza la shell grafica server, questa limitazione deve essere documentata e all'amministratore del server deve essere richiesto di installare la shell grafica server. Se si aggiunge a un'installazione Server Core, potrebbe essere necessario aggiungere funzionalità con funzionalità su richiesta. Inoltre, l'app deve verificare all'avvio che tutti i file necessari siano disponibili, perché la shell grafica server può essere disinstallata in qualsiasi momento prima o dopo l'installazione dell'app.

## <a name="solution"></a>Soluzione

Si basano sul minor numero possibile di dipendenze e sulle app modularizzare in modo che la funzionalità di base dell'app possa funzionare senza richiedere l'installazione di altri componenti dell'interfaccia utente. Sviluppare app che non richiedono le API o i file binari rimossi e si basano invece sulle funzionalità contenute nell'interfaccia server minima o in Server Core. Questa operazione ridurrà i requisiti di manutenzione migliorando le prestazioni e la soddisfazione degli utenti.

Laddove sono presenti parti di un'app che potrebbero aggiungere funzionalità significative quando la shell grafica server è disponibile, gli sviluppatori di app possono:

-   Consentire l'installazione facoltativa di queste funzionalità aggiuntive che usano la shell grafica server, in modo che possano essere omesse dalle installazioni in una configurazione di interfaccia server minima
-   Rileva la presenza della shell grafica server e adatta il comportamento dell'app

Gli sviluppatori di app devono inoltre assicurarsi che le app Server siano gestibili in remoto laddove possibile e appropriato.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Rilevamento dell'interfaccia server minima e del server core

Windows Server installerà un valore del registro di sistema corrispondente per ogni livello server installato. È possibile eseguire una query per l'esistenza di queste chiavi per determinare se le funzionalità della shell grafica server o dell'interfaccia server minima sono installate e abilitate.

HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ server \\ ServerLevels:



|                  | Server Core | Interfaccia server minima | Shell grafica server |
|------------------|-------------|--------------------------|------------------------|
| ServerCore = 1     | X           | X                        | X                      |
| Server-GuiMgmt = 1 |             | X                        | X                      |
| ServerGuiShell = 1 |             |                          | X                      |



 

Una "X" nella tabella precedente indica che la chiave del registro di sistema sarà presente quando viene installata la funzionalità corrispondente.

Si noti che questi livelli di server sono additivi; Se la shell grafica server è installata, è quindi l'interfaccia server minima e i componenti di base del server. In tal caso, saranno presenti entrambe le chiavi del registro di sistema.

## <a name="tests"></a>Test

Esaminare il codice dell'app per individuare i requisiti che usano le API e i file binari rimossi. Dopo aver rimosso tutte le istanze di questi file dai file binari dell'applicazione principale, testare l'app in un ambiente che non includa la shell grafica server. Strumenti come il monitoraggio dei processi potrebbero risultare utili per questa operazione.

Se non è possibile interrompere completamente l'uso di queste API e file binari, assicurarsi che l'app abbia esito negativo correttamente quando viene eseguita in un'interfaccia server minima o in Server Core.

## <a name="resources"></a>Risorse

-   [Documentazione di base del server esistente su MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 