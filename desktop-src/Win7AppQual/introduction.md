---
description: Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb61f41644f74e22f8e4117854db90cc1bea025b3ff5399819eaa580eee39f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994921"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

In tutto il mondo, molte aziende stanno adottando Windows 7 a causa delle funzionalità e delle capacità aziendali. I reparti IT stanno anche cambiando il modo in cui si avvicinano alle esigenze della piattaforma a lungo termine per supportare un desktop moderno. Il Windows 7 consente di ridurre il costo totale di proprietà consentendo agli utenti di rimanere produttivi ovunque, migliorare la sicurezza e il controllo e semplificare la gestione dei desktop in tutta l'organizzazione. Windows 7 include anche un browser moderno basato su standard, Windows Internet Explorer 8, che offre funzionalità di sicurezza e esplorazione migliorate. Queste due piattaforme aumentano l'efficienza IT e migliorano l'agilità e la sicurezza di un'organizzazione.

Tuttavia, la migrazione a un nuovo sistema operativo crea sfide specifiche, principalmente con la necessità di supportare le applicazioni Web legacy. Le aziende possono avere applicazioni create per le versioni precedenti di Windows Internet Explorer, ad esempio Windows Internet Explorer 7 o Microsoft Internet Explorer 6. Queste applicazioni Web possono riscontrare problemi di compatibilità con Internet Explorer 8. Inoltre, Internet Explorer 6 non viene eseguito in modo nativo in Windows 7 e Windows non supporta l'esecuzione di due versioni di Internet Explorer contemporaneamente. Per altre informazioni, vedere l'Microsoft Knowledge Base " Running[Multiple Versions of Internet Explorer on Single Operating System is Unsupported](https://support.microsoft.com/kb/2020599).

Molte aziende usano ancora Internet Explorer web basate su 6 che sono state create e personalizzate nel corso dell'ultimo decennio. Le aziende che pianificano la Windows 7 devono disporre di una strategia completa e di un piano di esecuzione per eseguire la migrazione di applicazioni Web legacy a Internet Explorer 8. Questo documento offre una panoramica dettagliata dei problemi di compatibilità Internet Explorer 8, illustra come eseguire la migrazione delle applicazioni Web e introduce gli strumenti e i processi correlati.

La Internet Explorer 8 è incentrata su tre temi principali:

-   Garantire l'interoperabilità reale con altri browser e la compatibilità per i siti Web esistenti.
-   È possibile velocizzare e semplificare lo sviluppo Web usando gli strumenti di sviluppo predefiniti.
-   Abilitare esperienze che vanno oltre la pagina, tramite nuove funzionalità del browser che connettono gli utenti a servizi Web innovative.

Oltre ai progressi significativi nel supporto degli standard, Internet Explorer 8 contiene ulteriori investimenti per la piattaforma per gli sviluppatori. Internet Explorer 8 migliora le prestazioni in molti sottosistemi Internet Explorer, ad esempio il parser HTML, l'elaborazione delle regole CSS (Cascading Style Sheet), la manipolazione dell'albero di markup, il parser JavaScript, il runtime del Garbage Collector e la gestione della memoria. Gli investimenti aggiuntivi per gli sviluppatori includono:

-   CSS 2.1: è possibile scrivere le pagine una sola volta e renderle più facilmente visualizzabili in browser diversi, perché Internet Explorer 8 supporta completamente la specifica CSS 2.1.
-   Document Object Model (DOM) e HTML 4.01: Internet Explorer 8 offre miglioramenti aggiuntivi per HTML 4.01 e conformità a CSS 2.1 completa. Internet Explorer 8 corregge anche molte incoerenze tra browser. Ad esempio, l'implementazione dell'attributo get/set/remove è ora interoperativizzabile con altri browser e le prestazioni sono migliorate negli schemi progettuali asincroni JavaScript e XML (AJAX).
-   Standard emergenti: Internet Explorer 8 incorpora standard futuri, ad esempio lo standard HTML5 Draft DOM Archiviazione di W3C, l'API dei selettori del gruppo di lavoro delle applicazioni Web e la sintassi approvata da ECMAScript 3.1.
-   Nuove funzionalità di navigazione per le applicazioni AJAX: è possibile aggiornare lo stack di navigazione in avanti e indietro del browser e la barra degli indirizzi da un'applicazione AJAX in modo che tali funzionalità del browser funzionino correttamente nell'applicazione.
-   Acid2: Internet Explorer 8 esegue correttamente il rendering del test del browser Acid2.
-   Compatibilità: Internet Explorer 8 include un motore di layout più compatibile con gli standard che consente di creare un sito basato su standard per più browser. Per eseguire più facilmente la migrazione dei siti al nuovo motore di layout conforme agli standard, Internet Explorer 8 consente di usare il motore di layout di Internet Explorer 7 inserendo un semplice **meta-elemento** nel codice o aggiungendo una singola intestazione HTTP nei server.
-   Strumenti di sviluppo: Strumenti di sviluppo in Internet Explorer ,a cui si accede premendo F12, è possibile eseguire rapidamente il debug di codice HTML, CSS e JavaScript in un ambiente visivo. Questi strumenti sono inclusi direttamente in Internet Explorer 8 con funzionalità espanse, inclusa un'opzione per scegliere l'applicazione da usare quando si visualizza l'origine di una pagina Web. È possibile identificare e risolvere rapidamente i problemi a causa delle informazioni approfondite fornite nello strumento nel DOM.
-   Per altre informazioni sulle funzionalità nuove e migliorate di Internet Explorer 8, vedere Novità [di Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



