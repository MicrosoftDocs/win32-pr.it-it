---
description: In questa sezione vengono fornite indicazioni per l'integrazione e l'estensione delle funzionalità per l'utente desktop di Windows.
ms.assetid: 1ffeeb4f-b337-45b9-885f-307b81670557
title: Ambiente desktop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb60457f700489ca4e9e7368425df380f8d10d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306692"
---
# <a name="desktop-environment"></a>Ambiente desktop

In questa sezione vengono fornite indicazioni per l'integrazione e l'estensione delle funzionalità per l'utente desktop di Windows. È possibile apprendere come garantire che le app e i formati di file vengano visualizzati e si comportino correttamente in Start, nella barra delle applicazioni, sul desktop e in Esplora file. È anche possibile garantire che i formati di file e gli archivi dati siano indicizzabili e ricercabili.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shell di Windows](./shell/shell-entry.md)<br/>                                      | L'interfaccia utente di Windows Desktop consente agli utenti di accedere a un'ampia gamma di oggetti necessari per l'esecuzione di applicazioni e la gestione del sistema operativo. I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer. Sono inoltre disponibili numerosi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file alle stampanti remote o l'accesso al Cestino. La shell organizza questi oggetti in uno spazio dei nomi gerarchico e fornisce a utenti e applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.<br/> |
| [Sistema di proprietà di Windows](./properties/windows-properties-system.md)<br/>         | Il sistema di proprietà di Windows è un sistema di lettura/scrittura estendibile di definizioni dei dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell. Il sistema di proprietà di Windows consente di archiviare e recuperare metadati per gli elementi della shell. Un elemento della shell è costituito da qualsiasi singolo contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto. Una proprietà è una singola parte di metadati associata a un elemento della shell.<br/>                                                                                                                                                                             |
| [Windows Search](./search/windows-search.md)<br/>                                 | Windows Search è una piattaforma di ricerca desktop con funzionalità di ricerca immediata per la maggior parte dei tipi di file e dati comuni, ad esempio posta elettronica, contatti, appuntamenti del calendario, documenti, foto, elementi multimediali e altri formati che possono essere estesi da sviluppatori di terze parti. Queste funzionalità consentono agli utenti di trovare, gestire e organizzare la maggiore quantità di dati comuni negli ambienti domestici e aziendali.<br/>                                                                                                                                                                                    |
| [Stazioni e desktop della finestra](./winstation/window-stations-and-desktops.md)<br/> | Windows offre tre categorie principali di oggetti: interfaccia utente, GDI (Graphics Device Interface) e kernel. Gli oggetti kernel sono entità a protezione diretta, mentre gli oggetti utente e gli oggetti GDI non lo sono. Pertanto, per fornire sicurezza aggiuntiva, gli oggetti dell'interfaccia utente vengono gestiti mediante le stazioni di Windows e i desktop, che a loro volta sono oggetti a protezione diretta.<br/>                                                                                                                                                                                                                                              |
| [Guida di Windows](/windows/win32/api/winuser/nf-winuser-winhelpa)<br/>                                        | Descrive le tecnologie di guida disponibili in Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [Console](/windows/console/character-mode-applications)<br/>                        | Le console di gestiscono l'input e l'output (I/O) per le applicazioni in modalità carattere (applicazioni che non forniscono una propria interfaccia utente grafica).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo dell'interfaccia utente dell'applicazione Windows](./windows-application-ui-development.md)
</dt> </dl>

 

 
