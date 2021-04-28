---
description: Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4125c2bd122d239c155f089f06bef2f455ee121b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088199"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

In tutto il mondo, molte aziende adottano Windows 7 grazie alle funzionalità e alle capacità aziendali. I reparti IT stanno anche cambiando il modo in cui si avvicinano alle esigenze della piattaforma a lungo termine per supportare un desktop moderno. Il sistema operativo Windows 7 consente di ridurre il costo totale di proprietà consentendo agli utenti di rimanere produttivi ovunque, migliorare la sicurezza e il controllo e semplificare la gestione dei desktop in tutta l'organizzazione. Windows 7 include anche un browser moderno basato su standard, Windows Internet Explorer 8, che offre sicurezza e funzionalità di esplorazione migliorate. Queste due piattaforme aumentano l'efficienza IT e migliorano l'agilità e la sicurezza di un'organizzazione.

Tuttavia, la migrazione a un nuovo sistema operativo crea sfide specifiche, principalmente con la necessità di supportare le applicazioni Web legacy. Le aziende possono avere applicazioni create per le versioni precedenti di Windows Internet Explorer, ad esempio Windows Internet Explorer 7 o Microsoft Internet Explorer 6. Queste applicazioni Web possono riscontrare problemi di compatibilità con Internet Explorer 8. Inoltre, Internet Explorer 6 non viene eseguito in modo nativo in Windows 7 e Windows non supporta l'esecuzione di due versioni di Internet Explorer contemporaneamente. Per altre informazioni, vedere l'Microsoft Knowledge Base " Running[Multiple Versions of Internet Explorer on Single Operating System is Unsupported](https://support.microsoft.com/kb/2020599).

Molte aziende usano ancora Internet Explorer web basate su 6 che sono state create e personalizzate nel corso dell'ultimo decennio. Le aziende che pianificano la distribuzione di Windows 7 devono disporre di una strategia completa e di un piano di esecuzione per eseguire la migrazione di applicazioni Web legacy a Internet Explorer 8. Questo documento offre una panoramica dettagliata di Internet Explorer 8 problemi di compatibilità, illustra come eseguire la migrazione di applicazioni Web e introduce strumenti e processi correlati.

La Internet Explorer 8 è incentrata su tre temi principali:

-   Fornire interoperabilità reale con altri browser e compatibilità per i siti Web esistenti.
-   Semplificare e velocizzare lo sviluppo Web usando gli strumenti di sviluppo predefiniti.
-   Abilitare esperienze che vanno oltre la pagina, tramite nuove funzionalità del browser che connettono gli utenti a servizi Web innovativi.

Oltre ai progressi significativi nel supporto degli standard, Internet Explorer 8 contiene investimenti aggiuntivi per la piattaforma per gli sviluppatori. Internet Explorer 8 migliora le prestazioni in molti sottosistemi Internet Explorer, ad esempio il parser HTML, l'elaborazione di regole CSS (Cascading Style Sheet), la manipolazione dell'albero di markup, il parser JavaScript, il runtime del Garbage Collector e la gestione della memoria. Altri investimenti per sviluppatori includono:

-   CSS 2.1: è possibile scrivere le pagine una sola volta e renderle più facilmente visualizzabili tra browser diversi, perché Internet Explorer 8 supporta completamente la specifica CSS 2.1.
-   Document Object Model (DOM) e HTML 4.01: Internet Explorer 8 offre miglioramenti aggiuntivi di HTML 4.01 e conformità completa a CSS 2.1. Internet Explorer 8 corregge anche molte incoerenze tra browser. Ad esempio, l'implementazione dell'attributo get/set/remove è ora interoperabile con altri browser e le prestazioni sono migliorate nei modelli di progettazione JavaScript e XML (AJAX) asincroni.
-   Standard emergenti: Internet Explorer 8 incorpora standard futuri, ad esempio lo standard HTML5 Draft DOM Storage di W3C, l'API Selettori del gruppo di lavoro applicazioni Web e la sintassi approvata da ECMAScript 3.1.
-   Nuove funzionalità di navigazione per le applicazioni AJAX: è possibile aggiornare lo stack di navigazione indietro e in avanti del browser e la barra degli indirizzi da un'applicazione AJAX in modo che tali funzionalità del browser funzionino correttamente nell'applicazione.
-   Acid2: Internet Explorer 8 esegue correttamente il rendering del test del browser Acid2.
-   Compatibilità: Internet Explorer 8 include un motore di layout più compatibile con gli standard che consente di creare un sito basato su standard per più browser. Per eseguire più facilmente la migrazione dei siti al nuovo motore di layout conforme agli standard, Internet Explorer 8 consente di usare il motore di layout di Internet Explorer 7 inserendo un semplice **meta-elemento** nel codice o aggiungendo una singola intestazione HTTP nei server.
-   Strumenti di sviluppo: Strumenti di sviluppo in Internet Explorer ,a cui si accede premendo F12, è possibile eseguire rapidamente il debug di codice HTML, CSS e JavaScript in un ambiente visivo. Questi strumenti sono inclusi direttamente in Internet Explorer 8 con funzionalità espanse, inclusa un'opzione per scegliere l'applicazione da usare quando si visualizza l'origine di una pagina Web. È possibile identificare e risolvere rapidamente i problemi a causa delle informazioni dettagliate che lo strumento fornisce nel DOM.
-   Per altre informazioni sulle funzionalità nuove e migliorate di Internet Explorer 8, vedere Novità [di Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



