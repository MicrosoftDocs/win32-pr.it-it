---
title: Windows Guide per gli sviluppatori del framework della barra multifunzione
description: Gli argomenti contenuti in questa sezione descrivono aspetti specifici del framework Windows ribbon.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows Barra multifunzione, framework
- Barra multifunzione, framework
- Windows Barra multifunzione, guide per sviluppatori
- Barra multifunzione, guide per sviluppatori
- Guide per gli sviluppatori per Windows barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850629"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows Guide per gli sviluppatori del framework della barra multifunzione

Gli argomenti contenuti in questa sezione descrivono aspetti specifici del framework Windows ribbon.

## <a name="basics"></a>Nozioni di base

[Creazione di un'applicazione barra multifunzione](windowsribbon-stepbystep.md)

Perché il framework Windows barra multifunzione sia in grado di utilizzare il file di markup della barra multifunzione, il file di markup deve essere compilato in un file di risorse in formato binario. Un compilatore di markup della barra multifunzione dedicato, UICC (UI Command Compiler), è incluso in Microsoft Windows Software Development Kit (SDK) (7.0 o versione successiva) a questo scopo. Oltre a compilare la versione binaria del markup della barra multifunzione, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse immagine e stringa all'applicazione host in fase di compilazione.

[Migrazione al framework Windows Ribbon](ribbon-migration.md)

È possibile eseguire la migrazione di un'applicazione basata su menu, barre degli strumenti e finestre di dialogo tradizionali all'interfaccia utente rich, dinamica e basata sul contesto del sistema di comandi del framework della barra multifunzione. Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle funzionalità.

[Informazioni su comandi e controlli](windowsribbon-commandscontrols.md)

La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi del framework della barra multifunzione, un sistema basato su uno schema progettuale in cui funzionalità e comportamento vengono implementati indipendentemente dai controlli che espongono questa funzionalità.

## <a name="user-interface"></a>Interfaccia utente

[Specifica delle risorse immagine della barra multifunzione](windowsribbon-imageformats.md)

Come sistema di presentazione dei comandi completo, il framework della barra multifunzione è progettato per supportare ampiamente le risorse immagine in tutta l'interfaccia utente della barra multifunzione. Tutte le risorse immagine vengono dichiarate nel [markup della barra multifunzione o](windowsribbon-schema.md) vengono sottoposti a query da un'applicazione host della barra multifunzione.

Per Windows 8 e versioni successive, il framework della barra multifunzione supporta i formati grafici seguenti: file bitmap ARGB (BMP) a 32 bit e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse immagine devono essere conformi al formato grafico BMP standard usato in Windows.

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)

I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione e in base a una combinazione di comportamenti predefiniti e modelli di layout (sia definiti dal framework che personalizzati) dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti del layout adattivo del framework della barra multifunzione che influiscono sul modo in cui i controlli nella barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.

[Uso delle raccolte](ribbon-controls-galleries.md)

Il framework della barra multifunzione offre agli sviluppatori un modello affidabile e coerente per la gestione del contenuto dinamico in un'ampia gamma di controlli basati su raccolte. Adattando e riconfigurando l'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione stessa e offrono la flessibilità necessaria per gestire vari ambienti di esecuzione.

[Visualizzazione delle schede contestuali](ribbon-contextualtabs.md)

In un'applicazione del framework della [](windowsribbon-controls-tab.md) barra multifunzione, una scheda contestuale è un controllo Struttura a schede nascosto che viene visualizzato nella riga della scheda quando un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine, viene selezionato o evidenziato.

[Riconfigurazione della barra multifunzione con le modalità dell'applicazione](ribbon-applicationmodes.md)

Il framework della barra multifunzione supporta la riconfigurazione dinamica e l'esposizione di elementi principali dell'interfaccia utente della barra multifunzione in fase di esecuzione, in base allo stato dell'applicazione (detto anche contesto). Dichiarati e associati a elementi specifici nel markup, i vari stati supportati da un'applicazione sono definiti modalità dell'applicazione.

[Personalizzazione dei colori della barra multifunzione](ribbon-color.md)

Il framework della barra multifunzione espone un set di proprietà di colore che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.

[Visualizzazione della barra multifunzione](ribbon-visibility.md)

Il framework della barra multifunzione espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.

## <a name="management"></a>Gestione

[Persistenza dello stato della barra multifunzione](ribbon-statepersistence.md)

Il Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.

[Ascolto di eventi della barra multifunzione](listening-for-ribbon-events.md)

Il framework della barra multifunzione usa [l'infrastruttura ETW (Event Tracing for Windows)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere come gli utenti interagiscono con la barra multifunzione dell'applicazione.

## <a name="markup-compiler"></a>Compilatore di markup

[Compilazione del markup della barra multifunzione](windowsribbon-intentcl.md)

Per usare il file di [markup della](windowsribbon-schema.md) barra multifunzione, il framework della barra multifunzione deve essere compilato in un file di risorse in formato binario. Un compilatore di markup dedicato, UICC (UI Command Compiler), è incluso in Microsoft Windows Software Development Kit (SDK) (7.0 o versione successiva) a questo scopo. Oltre a compilare la versione binaria del markup, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse immagine e stringa all'applicazione host in fase di compilazione.

[Informazioni sui messaggi del compilatore di markup](windowsribbon-compilationerrors.md)

Il compilatore di markup del framework della barra multifunzione di Windows, il compilatore di comandi dell'interfaccia utente (UICC.exe), convalida il markup della barra multifunzione rispetto allo schema della barra multifunzione e a un set aggiuntivo di regole definite dal framework della barra multifunzione.

 

 