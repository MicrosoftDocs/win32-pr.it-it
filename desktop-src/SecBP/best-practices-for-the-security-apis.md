---
description: Suggerimenti per le valutazioni della sicurezza delle applicazioni per lo sviluppo di app Windows software di sicurezza e sviluppo di software sicuro, inclusi i test di sicurezza delle applicazioni.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Procedure consigliate per le API di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934bf52d99456d599f91ec23c6e5472bb4e130565cf1acb56763f29f6396c0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622881"
---
# <a name="best-practices-for-the-security-apis"></a>Procedure consigliate per le API di sicurezza

Per sviluppare software sicuro, è consigliabile usare le procedure consigliate seguenti per lo sviluppo di applicazioni. Per altre informazioni, vedere [Centro per sviluppatori per la sicurezza](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Ciclo di vita dello sviluppo della sicurezza

Il [ciclo di vita](/previous-versions/ms995349(v=msdn.10)) di sviluppo della sicurezza (SDL) è un processo che allinea una serie di attività e risultati finali incentrati sulla sicurezza a ogni fase dello sviluppo software. Queste attività e risultati finali includono:

-   Sviluppo di modelli di minaccia
-   Uso degli strumenti di analisi del codice
-   Esecuzione di verifiche del codice e test di sicurezza

Per altre informazioni su SDL, vedere il [blog di SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelli di minaccia

L'esecuzione di un'analisi del modello di minaccia consente di individuare potenziali punti di attacco nel codice. Per altre informazioni sull'analisi del modello di minaccia, vedere Howard, Michael e LeBlanc, David \[ 2003, \] *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

## <a name="service-packs-and-security-updates"></a>Service Pack e aggiornamenti della sicurezza

Gli ambienti di compilazione e test devono rispecchiare gli stessi livelli di Service Pack e aggiornamenti della sicurezza della base di utenti di destinazione. È consigliabile installare i Service Pack e gli aggiornamenti della sicurezza più recenti per qualsiasi piattaforma o applicazione Microsoft che fa parte dell'ambiente di compilazione e test e invitare gli utenti a eseguire la stessa operazione per l'ambiente dell'applicazione completato. Per altre informazioni sui Service Pack e sugli aggiornamenti della sicurezza, vedere [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) e Microsoft [Security.](https://www.microsoft.com/security)

## <a name="authorization"></a>Autorizzazione

È consigliabile creare applicazioni che richiedono il privilegio minimo possibile. L'uso del privilegio meno possibile riduce il rischio di codice dannoso che compromette il sistema informatico. Per altre informazioni sull'esecuzione di codice con il livello di privilegio meno possibile, vedere [Esecuzione con privilegi speciali](running-with-special-privileges.md).

## <a name="more-information"></a>Altre informazioni

Per altre informazioni sulle procedure consigliate, vedere gli argomenti seguenti.



| Argomento                                                                                                                        | Descrizione                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Esecuzione con privilegi speciali](running-with-special-privileges.md)<br/>                                            | Vengono illustrate le implicazioni di sicurezza dei privilegi.<br/>                                                                                                                                  |
| [Evitare sovraccarichi del buffer](avoiding-buffer-overruns.md)<br/>                                                          | Fornisce informazioni su come evitare sovraccarichi del buffer.<br/>                                                                                                                            |
| [Control Flow Guard (CFG)](control-flow-guard.md)<br/>                                                                | Vengono illustrate le vulnerabilità di danneggiamento della memoria.<br/>                                                                                                                                    |
| [Creazione di un elenco DACL](creating-a-dacl.md)<br/>                                                                            | Viene illustrato come creare un elenco di controllo di accesso discrezionale (DACL) usando il linguaggio SDDL [(Security Descriptor Definition Language).](/windows/desktop/SecAuthZ/security-descriptor-definition-language)<br/> |
| [Gestione delle password](handling-passwords.md)<br/>                                                                      | Vengono illustrate le implicazioni di sicurezza dell'uso delle password.<br/>                                                                                                                             |
| [Come ottimizzare la ricerca in MSDN Library](how-to-optimize-your-msdn-library-search.md)<br/>                          | Vengono illustrate le opzioni per la ricerca del contenuto di Security SDK in MSDN Library.<br/>                                                                                                           |
| [Estendibilità dinamica degli sviluppatori di Controllo di accesso dinamico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientamento di base per alcuni dei punti di estendibilità per gli sviluppatori per le nuove soluzioni di controllo dinamico degli accessi.<br/>                                                                   |



 

 

