---
title: Informazioni sui comandi e sui controlli
description: La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi di Windows Ribbon Framework \ 8212; un sistema basato su uno schema progettuale in cui funzionalità e comportamento sono implementate indipendentemente dai controlli che espongono questa funzionalità.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Barra multifunzione di Windows, Panoramica comandi
- Barra multifunzione, Panoramica comandi
- Barra multifunzione di Windows, Cenni preliminari sui controlli
- Barra multifunzione, Cenni preliminari sui controlli
- sistema di comando per la barra multifunzione di Windows
- controlli per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566031"
---
# <a name="understanding-commands-and-controls"></a>Informazioni sui comandi e sui controlli

La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi del Framework della barra multifunzione di Windows, un sistema basato su uno schema progettuale in cui funzionalità e comportamento sono implementate indipendentemente dai controlli che espongono questa funzionalità.

-   [Introduzione](#introduction)
-   [Sistema di comandi della barra multifunzione di Windows](#the-windows-ribbon-command-system)
    -   [Controlli](#understanding-commands-and-controls)
    -   [Comandi](#understanding-commands-and-controls)
    -   [Esperienza del comando in azione](#the-command-experience-in-action)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Questo articolo illustra la progettazione del sistema di comandi del Framework della barra multifunzione. Vengono descritti i concetti di comandi e controlli ed è possibile esplorare il modo in cui interagiscono per offrire un'esperienza di comando avanzata con un host di nuove funzionalità dell'interfaccia utente.

## <a name="the-windows-ribbon-command-system"></a>Sistema di comandi della barra multifunzione di Windows

Nel framework della barra multifunzione, i comandi e i controlli sono entità indipendenti. Un comando è una struttura astratta, senza vincoli di presentazione, che rappresenta un'attività o una classe di funzionalità specifica. Un controllo, d'altra parte, è un oggetto concreto che espone la funzionalità del comando tramite l'interfaccia utente della barra multifunzione.

Questa distinzione consente di definire i comandi che sono privi di dettagli dell'interfaccia utente e possono essere eseguiti allo scopo di un'azione senza la necessità di gestire il modo in cui l'azione è stata richiamata.

### <a name="controls"></a>Controlli

I controlli sono gli oggetti dell'interfaccia utente necessari per la presentazione del comando. Viene eseguito il rendering e la gestione in fase di esecuzione dal Framework in base all'interazione dell'utente e a un set di proprietà e comportamenti intrinseci.

Noto come layout adattivo, la flessibilità gestita dal framework dell'interfaccia utente è uno degli ottimi punti di forza della barra multifunzione. I controlli della barra multifunzione possono essere riconfigurati automaticamente tramite modelli di layout dipendenti dal Framework o definiti dallo sviluppatore che sono in grado di rispondere a diversi requisiti del runtime, il tutto senza scrivere una singola riga di codice di presentazione. Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).

Oltre ai vantaggi del layout adattivo, molti controlli della barra multifunzione complessi forniscono soluzioni autosufficienti per spazi di problemi specifici dell'interfaccia utente. Grazie a un modello di interazione sofisticato, i controlli della barra multifunzione, ad esempio FontControl o ColorPicker, consentono di modificare i dati in termini più astratti tramite i contenitori di proprietà degli attributi dei tipi di carattere o dei colori effettivi anziché tramite vari controlli secondari, enumerazioni e valori di indice dei controlli Windows standard.

### <a name="commands"></a>Comandi

A regime di controllo libero ai controlli della barra multifunzione che espongono la loro funzionalità, le implementazioni dei comandi sono il dominio dell'applicazione host e hanno il formato di listener di eventi, gestori di comandi e varie proprietà del comando.

I comandi sono dichiarati nel markup della barra multifunzione con un ID univoco o assegnano un ID generato dal compilatore di markup durante la compilazione. I comandi sono associati ai controlli tramite un nome di comando ma, a differenza dei controlli, la relativa funzionalità effettiva viene definita nel codice in cui sono associati a gestori di comandi specifici tramite l'ID di comando.

> [!Note]  
> In fase di compilazione, questo ID viene archiviato in un file di intestazione della definizione di ID che espone i comandi ai gestori di comandi corrispondenti nell'applicazione host della barra multifunzione.

 

Ogni comando ha un tipo di comando sottostante nell'enumerazione [**\_ COMMANDTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .

### <a name="the-command-experience-in-action"></a>Esperienza del comando in azione

Le funzionalità di questo modello di comando sono illustrate dalla barra di accesso rapido della barra multifunzione (QAT). Il QAT offre agli utenti finali un modo per definire facilmente i propri collegamenti per qualsiasi controllo nell'interfaccia utente della barra multifunzione. Un collegamento viene aggiunto dinamicamente a QAT in fase di esecuzione quando l'utente fa clic con il pulsante destro del mouse su un controllo Ribbon e seleziona **Aggiungi alla barra di accesso rapido** dal menu di scelta rapida.

Nell'immagine seguente vengono illustrati i comandi **Incolla** e **Incolla da** , rappresentati da un controllo [**SplitButton**](windowsribbon-element-splitbutton.md) , nella barra multifunzione di Windows 7 Paint.

![immagine del SplitButton incolla nella barra multifunzione di Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

Nell'immagine seguente vengono mostrati gli stessi comandi **Incolla** e **Incolla** dei comandi, ancora rappresentati da un controllo [**SplitButton**](windowsribbon-element-splitbutton.md) , nella barra multifunzione qat di Windows 7 Paint.

![immagine del SplitButton incolla in Microsoft Paint qat.](images/overviews/paint-paste-splitbutton-qat.png)

Quando un controllo è ospitato da QAT, la nuova istanza del controllo mantiene tutte le funzionalità del controllo originale senza la necessità di altri listener di eventi e gestori di comandi per supportarla. Entrambi i controlli sono associati allo stesso gestore di comandi della barra multifunzione tramite un identificatore di comando condiviso. In questo modo, il Framework considera entrambi i controlli come uno, indipendentemente dal fatto che venga richiamato.

> [!Note]  
> Gli stessi vantaggi vengono realizzati quando i comandi vengono incorporati in un [**ContextPopup**](windowsribbon-element-contextpopup.md) in fase di progettazione. In questo caso, è possibile usare i gestori dei comandi di Incolla se il controllo [**SplitButton**](windowsribbon-element-splitbutton.md) viene visualizzato nella barra multifunzione, qat o **ContextPopup**.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione al framework della barra multifunzione di Windows](windowsribbon-introduction.md)
</dt> <dt>

[Creazione di un'applicazione Ribbon](windowsribbon-stepbystep.md)
</dt> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)
</dt> </dl>

 

 