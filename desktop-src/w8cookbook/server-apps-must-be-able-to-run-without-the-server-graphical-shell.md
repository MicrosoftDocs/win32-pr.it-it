---
title: Restrizioni della shell grafica del server
description: Le app server devono essere in grado di essere eseguite senza la shell grafica del server
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1742b87d0cb4ece4ac05b38b0ac2644967eee256931df5dfc8ec838574db33ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773187"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Le app server devono essere in grado di essere eseguite senza la shell grafica del server

## <a name="platform"></a>Piattaforma

**Server** : Windows Server 2012 

## <a name="description"></a>Descrizione

Shell grafica server, la funzionalità che include Windows Explorer e Internet Explorer, viene installata per impostazione predefinita nelle installazioni "Server con gui" di Windows Server 2012. La funzionalità Shell grafica server può essere disinstallata per ridurre il potenziale footprint di manutenzione e prestazioni, limitando così il numero di riavvii che possono verificarsi nel server, consentendo comunque l'esecuzione degli strumenti di gestione in locale nel server.

Dopo la disinstallazione di Shell grafica server da parte di un amministratore, il server è nella configurazione dell'interfaccia server minima:

![configurazione dell'interfaccia grafica della shell del server](images/minimalserverinterface.png)

Gli amministratori possono quindi scegliere di eseguire la configurazione dell'interfaccia server minima (che include un set di strumenti di gestione locali), come impostazione predefinita, anziché nel server con una configurazione GUI. Ciò consente il monitoraggio e la gestione locali, riducendo al tempo stesso l'utilizzo delle risorse e la frequenza di manutenzione.

Gli amministratori possono reinstallare Shell grafica server in un secondo momento se necessitano della funzionalità al suo interno. Gli amministratori possono anche iniziare da un'installazione dei componenti di base del server e "creare" la configurazione dell'interfaccia server minima usando la funzionalità Funzionalità su richiesta.

Le app server devono essere in grado di essere eseguite nella configurazione dell'interfaccia server minima per sfruttare la riduzione dell'utilizzo delle risorse e del footprint di manutenzione. Questa funzionalità può essere ottenuta consentendo all'amministratore di scegliere di non installare parti dell'app che hanno bisogno della shell grafica server o rilevando la presenza di Shell grafica server e disabilitando alcuni aspetti dell'app.

L'interfaccia server minima ha una riduzione delle risorse e del footprint di manutenzione perché molte API e file binari inclusi nella shell grafica del server non sono disponibili in questa configurazione. Se appropriato, le app server devono anche consentire l'amministrazione remota (preferibilmente tramite Windows PowerShell Remoting) da un'altra installazione Windows Server o Windows Client. Ciò consente un'amministrazione centralizzata migliore di uno o più computer nella configurazione Dell'interfaccia server minima o di computer in una configurazione con footprint ancora inferiore, ad esempio Server Core.

## <a name="manifestation"></a>Manifestazione

Se un'app richiede api o file binari non disponibili nella configurazione dell'interfaccia server minima, potrebbe non essere visualizzata correttamente sullo schermo e/o essere inutilizzabile.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli sviluppatori di app server devono identificare le parti delle app che richiedono le API o i file binari rimossi e includere informazioni per l'amministratore del server che identificano le parti dell'app che non verranno eseguite correttamente quando si usa l'interfaccia server minima. Se queste parti dell'app possono essere installate facoltativamente o non sono assolutamente necessarie per la funzionalità del prodotto, l'app può comunque essere installata ed eseguita con la configurazione Dell'interfaccia server minima.

Se l'app non può essere usata affatto senza La shell grafica server, questa limitazione deve essere documentata e all'amministratore del server deve essere richiesto di installare La shell grafica server. Se si aggiunge a un'installazione Server Core, potrebbe essere necessario aggiungere funzionalità usando funzionalità su richiesta. Inoltre, l'app deve verificare all'avvio che tutti i file necessari siano disponibili, perché La shell grafica server può essere disinstallata in qualsiasi momento prima o dopo l'installazione dell'app.

## <a name="solution"></a>Soluzione

Basarsi sul set più piccolo possibile di dipendenze e modularizzare le app in modo che le funzionalità principali dell'app possano funzionare senza richiedere l'installazione di componenti dell'interfaccia utente più pesanti. Sviluppare app che non richiedono api o file binari rimossi e si basano invece sulle funzionalità contenute nell'interfaccia server minima o in Server Core. Ciò ridurrà i requisiti di manutenzione migliorando al tempo stesso le prestazioni e la soddisfazione degli utenti.

Se sono presenti parti di un'app che potrebbero aggiungere funzionalità significative quando è disponibile la shell grafica server, gli sviluppatori di app possono:

-   Consentire l'installazione facoltativa di queste funzionalità aggiuntive che usano Shell grafica server, in modo che possano essere omesse dalle installazioni in una configurazione dell'interfaccia server minima
-   Rilevare la presenza di Shell grafica server e adattare il comportamento dell'app

Gli sviluppatori di app devono anche assicurarsi che le app server siano gestibili in remoto, laddove possibile e appropriato.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Rilevamento dell'interfaccia server minima e dei componenti di base del server

Windows Il server installerà un valore del Registro di sistema corrispondente per ogni livello server installato. È possibile eseguire una query per verificare l'esistenza di queste chiavi per determinare se le funzionalità Shell grafica server o Interfaccia server minima sono installate e abilitate.

HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ \\ ServerLevels:



|   &nbsp;         | Server Core | Interfaccia server minima | Shell grafica server |
|------------------|-------------|--------------------------|------------------------|
| ServerCore=1     | X           | X                        | X                      |
| Server-GuiMgmt=1 |             | X                        | X                      |
| ServerGuiShell=1 |             |                          | X                      |



 

Una "X" nella tabella precedente indica che la chiave del Registro di sistema sarà presente quando viene installata la funzionalità corrispondente.

Si noti che questi livelli di server sono additivi. se è installata la shell grafica del server, lo sono anche l'interfaccia server minima e i componenti di base del server. In tal caso, saranno presenti entrambe le chiavi del Registro di sistema.

## <a name="tests"></a>Test

Esaminare il codice dell'app per i requisiti che usano le API e i file binari rimossi. Dopo aver rimosso le istanze di questi file dai file binari "core application", testare l'app in un ambiente che non include la shell grafica del server. Strumenti come Process Monitor possono essere utili a questo scopo.

Se non è possibile interrompere completamente l'uso di queste API e file binari, assicurarsi che l'app non funzioni correttamente quando viene eseguita nell'interfaccia server minima o in Server Core.

## <a name="resources"></a>Risorse

-   [Documentazione di Server Core esistente su MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 