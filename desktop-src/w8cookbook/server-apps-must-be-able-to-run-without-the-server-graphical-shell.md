---
title: Restrizioni della shell grafica del server
description: Le app server devono essere in grado di essere eseguite senza Shell grafica server
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443222"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Le app server devono essere in grado di essere eseguite senza Shell grafica server

## <a name="platform"></a>Piattaforma

**Server** - Windows Server 2012 

## <a name="description"></a>Descrizione

Server Graphical Shell, la funzionalità che include Esplora risorse e Internet Explorer, viene installata per impostazione predefinita nelle installazioni "Server con un'interfaccia utente grafica" di Windows Server 2012. La funzionalità Shell grafica server può essere disinstallata per ridurre il potenziale footprint di manutenzione e prestazioni, limitando così il numero di riavvii che il server può eseguire, pur consentendo l'esecuzione locale degli strumenti di gestione nel server.

Dopo la disinstallazione di Server Graphical Shell da parte di un amministratore, il server è nella configurazione dell'interfaccia server minima:

![configurazione dell'interfaccia della shell grafica del server](images/minimalserverinterface.png)

Gli amministratori possono quindi scegliere di eseguire nella configurazione dell'interfaccia server minima (che include un set di strumenti di gestione locali), come impostazione predefinita, anziché nel server con una configurazione GUI. Ciò consente il monitoraggio e la gestione locali, riducendo al tempo stesso l'utilizzo delle risorse e la frequenza di manutenzione.

Gli amministratori possono reinstallare Server Graphical Shell in un secondo momento se hanno bisogno della funzionalità al suo interno. Gli amministratori possono anche iniziare da un'installazione server core e dalla configurazione dell'interfaccia server minima usando la funzionalità Funzionalità su richiesta.

Le app server devono essere in grado di essere eseguite nella configurazione dell'interfaccia server minima per sfruttare il footprint ridotto di utilizzo e manutenzione delle risorse. Questa funzionalità può essere ottenuta consentendo all'amministratore di scegliere di non installare parti dell'app che hanno bisogno di Shell grafica server o rilevando la presenza di Shell grafica server e disabilitando alcuni aspetti dell'app.

L'interfaccia server minima ha un footprint ridotto di risorse e manutenzione perché molte API e file binari inclusi in Shell grafica server non sono disponibili in questa configurazione. Se appropriato, le app server devono consentire anche l'amministrazione remota (preferibilmente tramite Windows PowerShell remota) da un'altra installazione di Windows Server o client Windows. Ciò consente una migliore amministrazione centralizzata di uno o più computer nella configurazione dell'interfaccia server minima o di computer in una configurazione con footprint ancora inferiore, ad esempio Server Core.

## <a name="manifestation"></a>Manifestazione

Se un'app richiede api o file binari non disponibili nella configurazione dell'interfaccia server minima, potrebbe non essere visualizzata correttamente sullo schermo e/o essere inutilizzabile.

## <a name="mitigation"></a>Mitigazione

Gli sviluppatori di app server devono identificare le parti delle app che richiedono le API o i file binari rimossi e includere informazioni per l'amministratore del server che identifica le parti dell'app che non verranno eseguite correttamente quando si usa l'interfaccia server minima. Se queste parti dell'app possono essere installate facoltativamente o non sono assolutamente necessarie per la funzionalità del prodotto, l'app può comunque essere installata ed eseguita con la configurazione dell'interfaccia server minima.

Se l'app non può essere usata affatto senza Server Graphical Shell, questa limitazione deve essere documentata e all'amministratore del server deve essere richiesto di installare La shell grafica del server. Se si aggiunge a un'installazione Server Core, potrebbe essere necessario aggiungere funzionalità tramite funzionalità su richiesta. Inoltre, l'app deve verificare all'avvio che siano disponibili tutti i file necessari, in quanto Server Graphical Shell può essere disinstallato in qualsiasi momento prima o dopo l'installazione dell'app.

## <a name="solution"></a>Soluzione

Basarsi sul più piccolo set possibile di dipendenze e modularizzare le app in modo che le funzionalità principali dell'app possano funzionare senza richiedere componenti dell'interfaccia utente più pesanti installati. Sviluppare app che non richiedono API o file binari rimossi e si basano invece sulle funzionalità contenute nell'interfaccia server minima o in Server Core. Ciò ridurrà i requisiti di manutenzione, migliorando al tempo stesso le prestazioni e la soddisfazione degli utenti.

Se sono presenti parti di un'app che potrebbero aggiungere funzionalità significative quando è disponibile Server Graphical Shell, gli sviluppatori di app possono:

-   Consentire l'installazione facoltativa di queste funzionalità aggiuntive che usano Shell grafica server, in modo che possano essere omesse dalle installazioni in una configurazione minima dell'interfaccia server
-   Rilevare la presenza di Shell grafica server e adattare il comportamento dell'app

Gli sviluppatori di app devono anche garantire che le app server siano gestibili in remoto, laddove possibile e appropriato.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Rilevamento dell'interfaccia server minima e dei componenti di base del server

Windows Server installerà un valore del Registro di sistema corrispondente per ogni livello di server installato. È possibile eseguire una query per verificare l'esistenza di queste chiavi per determinare se le funzionalità Shell grafica server o Interfaccia server minima sono installate e abilitate.

HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels:



|   &nbsp;         | Server Core | Interfaccia server minima | Shell grafica server |
|------------------|-------------|--------------------------|------------------------|
| ServerCore=1     | X           | X                        | X                      |
| Server-GuiMgmt=1 |             | X                        | X                      |
| ServerGuiShell=1 |             |                          | X                      |



 

Una "X" nella tabella precedente indica che la chiave del Registro di sistema sarà presente quando viene installata la funzionalità corrispondente.

Si noti che questi livelli di server sono additivi. se è installata La shell grafica del server, anche l'interfaccia server minima e Server Core. In tal caso, saranno presenti entrambe le chiavi del Registro di sistema.

## <a name="tests"></a>Test

Esaminare il codice dell'app per i requisiti che usano le API e i file binari rimossi. Dopo aver rimosso tutte le istanze di queste istanze dai file binari "core application", testare l'app in un ambiente che non include La shell grafica del server. Strumenti come Monitoraggio processi possono essere utili per questo scopo.

Se non è possibile interrompere completamente l'uso di queste API e file binari, assicurarsi che l'app non riesca correttamente quando viene eseguita in Minimal Server Interface o Server Core.

## <a name="resources"></a>Risorse

-   [Documentazione di Server Core esistente su MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 