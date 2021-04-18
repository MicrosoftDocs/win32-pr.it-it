---
description: .
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d491802735ddf1ef75a7a183cd49afea2cc657b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313698"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introduzione (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

In tutto il mondo, molte aziende adottano Windows 7 a causa delle caratteristiche e delle capacità aziendali. I reparti IT cambiano anche il modo in cui si avvicinano alla piattaforma a lungo termine che deve supportare un desktop moderno. Il sistema operativo Windows 7 contribuisce a ridurre il costo totale di proprietà aiutando gli utenti a rimanere produttivi ovunque, a migliorare la sicurezza e il controllo e a semplificare la gestione dei desktop nell'intera organizzazione. Windows 7 include inoltre un browser moderno basato su standard, Windows Internet Explorer 8, che offre funzionalità migliorate per la sicurezza e l'esplorazione avanzata. Queste due piattaforme aumentano l'efficienza IT e migliorano la flessibilità e la sicurezza di un'organizzazione.

Tuttavia, la migrazione a un nuovo sistema operativo crea problemi univoci, principalmente con la necessità di supportare le applicazioni Web legacy. Le aziende possono disporre di applicazioni compilate per le versioni precedenti di Windows Internet Explorer, ad esempio Windows Internet Explorer 7 o Microsoft Internet Explorer 6. Queste applicazioni Web potrebbero riscontrare problemi di compatibilità con Internet Explorer 8. Internet Explorer 6 non è inoltre eseguito in modo nativo in Windows 7 e Windows non supporta contemporaneamente l'esecuzione di due versioni di Internet Explorer. Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base "[esecuzione di più versioni di Internet Explorer in un singolo sistema operativo non supportata](https://support.microsoft.com/kb/2020599)".

Molte aziende usano ancora applicazioni Web basate su Internet Explorer 6 compilate e personalizzate negli ultimi decenni. Le aziende che pianificano di distribuire Windows 7 devono disporre di una strategia completa e di un piano di esecuzione per eseguire la migrazione di applicazioni Web legacy a Internet Explorer 8. In questo documento viene fornita una panoramica dettagliata dei problemi di compatibilità di Internet Explorer 8, viene illustrato come eseguire la migrazione di applicazioni Web e vengono introdotti gli strumenti e i processi correlati.

La versione di Internet Explorer 8 è stata incentrata su tre temi principali:

-   Fornire l'interoperabilità reale con altri browser e la compatibilità per i siti Web esistenti.
-   Semplifica e velocizza lo sviluppo Web usando gli strumenti di sviluppo predefiniti.
-   Grazie alle nuove funzionalità del browser che connettono gli utenti ai servizi Web innovativi, è possibile abilitare esperienze che raggiungono la pagina oltre la pagina.

Oltre ai significativi progressi del supporto per gli standard, Internet Explorer 8 contiene ulteriori investimenti della piattaforma per gli sviluppatori. Internet Explorer 8 migliora le prestazioni in molti sottosistemi di Internet Explorer, ad esempio il parser HTML, l'elaborazione delle regole CSS (CSS), la manipolazione degli alberi di markup, il parser JavaScript, il runtime Garbage Collector e la gestione della memoria. Gli investimenti aggiuntivi per gli sviluppatori includono:

-   CSS 2,1: è possibile scrivere le pagine una volta e visualizzarle in modo più semplice in browser diversi, poiché Internet Explorer 8 supporta completamente la specifica CSS 2,1.
-   Miglioramenti di Document Object Model (DOM) e HTML 4,01: Internet Explorer 8 fornisce miglioramenti aggiuntivi in HTML 4,01 e la conformità completa CSS 2,1. Internet Explorer 8 corregge anche molte incoerenze tra browser. Ad esempio, l'implementazione dell'attributo get/set/Remove è ora interoperativa con altri browser e le prestazioni sono migliorate nei modelli di progettazione AJAX (Asynchronous JavaScript and XML).
-   Standard emergenti: Internet Explorer 8 incorpora standard futuri, ad esempio W3C HTML5 Draft DOM standard, l'API dei selettori del gruppo di lavoro delle applicazioni Web e la sintassi di ECMAScript 3,1 approvata.
-   Nuove funzionalità di navigazione per le applicazioni AJAX: è possibile aggiornare lo stack di navigazione e la barra degli indirizzi del browser dalle applicazioni AJAX in modo che le funzionalità del browser funzionino correttamente nell'applicazione.
-   Acid2: Internet Explorer 8 esegue il rendering del test del browser Acid2 correttamente.
-   Compatibilità: Internet Explorer 8 include un motore di layout più compatibile con gli standard che consente di creare un sito basato su standard per più browser. Per eseguire la migrazione dei siti più facilmente al nuovo motore di layout conforme agli standard, Internet Explorer 8 consente di utilizzare il motore di layout di Internet Explorer 7 inserendo un semplice elemento **meta** nel codice o aggiungendo una singola intestazione HTTP nei server.
-   Strumenti di sviluppo: Strumenti di sviluppo in Internet Explorer (a cui si accede premendo il tasto F12) consente di eseguire rapidamente il debug del codice HTML, CSS e JavaScript in un ambiente visivo. Questi strumenti sono inclusi direttamente in Internet Explorer 8 con funzionalità espanse, tra cui Ann option per scegliere l'applicazione da usare quando si visualizza l'origine di una pagina Web. È possibile identificare e risolvere rapidamente i problemi grazie alla profonda conoscenza fornita dallo strumento nel DOM.
-   Per ulteriori informazioni sulle funzionalità nuove e migliorate di Internet Explorer 8, vedere la pagina relativa alle [novità di Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



