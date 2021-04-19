---
description: Suggerimenti per la valutazione della sicurezza delle applicazioni per lo sviluppo di app del software di sicurezza di Windows e lo sviluppo di software sicuro, inclusi i test di sicurezza dell'applicazione
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Procedure consigliate per le API di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317745"
---
# <a name="best-practices-for-the-security-apis"></a>Procedure consigliate per le API di sicurezza

Per contribuire allo sviluppo di software protetto, è consigliabile utilizzare le seguenti procedure consigliate per lo sviluppo di applicazioni. Per ulteriori informazioni, vedere [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Ciclo di vita dello sviluppo della sicurezza

Il [ciclo di vita dello sviluppo della sicurezza](/previous-versions/ms995349(v=msdn.10)) (SDL) è un processo che allinea una serie di attività mirate alla sicurezza e risultati finali a ogni fase dello sviluppo del software. Queste attività e risultati finali includono:

-   Sviluppo di modelli di rischio
-   Uso degli strumenti di analisi del codice
-   Esecuzione di revisioni del codice e test di sicurezza

Per ulteriori informazioni sul processo SDL, vedere il [Blog SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelli di rischio

L'esecuzione di un'analisi del modello di minaccia può aiutare a individuare potenziali punti di attacco nel codice. Per altre informazioni sull'analisi del modello di minaccia, vedere Howard, Michael e LeBlanc, David \[ 2003 \] , *scrittura di codice sicuro*, 2D ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

## <a name="service-packs-and-security-updates"></a>Service Pack e aggiornamenti della sicurezza

Gli ambienti di compilazione e di test devono eseguire il mirroring degli stessi livelli di Service Pack e degli aggiornamenti della sicurezza della base utente di destinazione. Si consiglia di installare i Service Pack e gli aggiornamenti della sicurezza più recenti per qualsiasi piattaforma o applicazione Microsoft che fa parte dell'ambiente di compilazione e di test e incoraggiare gli utenti a eseguire la stessa operazione per l'ambiente dell'applicazione finito. Per ulteriori informazioni sui Service Pack e gli aggiornamenti della sicurezza, vedere [microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) e [Microsoft Security](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorizzazione

È necessario creare applicazioni che richiedono il minor privilegio possibile. L'utilizzo del privilegio meno possibile riduce il rischio che il codice dannoso compromettere il sistema del computer. Per ulteriori informazioni sull'esecuzione del codice in un livello di privilegio minimo, vedere [esecuzione con privilegi speciali](running-with-special-privileges.md).

## <a name="more-information"></a>Altre informazioni

Per ulteriori informazioni sulle procedure consigliate, vedere gli argomenti seguenti.



| Argomento                                                                                                                        | Descrizione                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Esecuzione con privilegi speciali](running-with-special-privileges.md)<br/>                                            | Illustra le implicazioni di sicurezza dei privilegi.<br/>                                                                                                                                  |
| [Evitare i sovraccarichi del buffer](avoiding-buffer-overruns.md)<br/>                                                          | Fornisce informazioni su come evitare i sovraccarichi del buffer.<br/>                                                                                                                            |
| [Guard flusso di controllo (CFG)](control-flow-guard.md)<br/>                                                                | Illustra le vulnerabilità di danneggiamento della memoria.<br/>                                                                                                                                    |
| [Creazione di un DACL](creating-a-dacl.md)<br/>                                                                            | Viene illustrato come creare un elenco di controllo di accesso discrezionale (DACL) utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).<br/> |
| [Gestione delle password](handling-passwords.md)<br/>                                                                      | Illustra le implicazioni di sicurezza dell'utilizzo delle password.<br/>                                                                                                                             |
| [Come ottimizzare la ricerca in MSDN Library](how-to-optimize-your-msdn-library-search.md)<br/>                          | Illustra le opzioni per la ricerca di contenuto SDK di sicurezza in MSDN Library.<br/>                                                                                                           |
| [Estendibilità degli sviluppatori per il controllo dinamico degli accessi](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientamento di base per alcuni dei punti di estendibilità degli sviluppatori per le nuove soluzioni di controllo dinamico degli accessi.<br/>                                                                   |



 

 

