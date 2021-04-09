---
title: Guide per gli sviluppatori di Windows Ribbon Framework
description: Gli argomenti contenuti in questa sezione descrivono aspetti specifici del Framework della barra multifunzione di Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Barra multifunzione di Windows, Framework
- Barra multifunzione, Framework
- Barra multifunzione di Windows, guide per sviluppatori
- Barra multifunzione, guide per sviluppatori
- Guide per sviluppatori per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118266"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Guide per gli sviluppatori di Windows Ribbon Framework

Gli argomenti contenuti in questa sezione descrivono aspetti specifici del Framework della barra multifunzione di Windows.

## <a name="basics"></a>Nozioni di base

[Creazione di un'applicazione Ribbon](windowsribbon-stepbystep.md)

Affinché il Framework della barra multifunzione di Windows utilizzi il file di markup della barra multifunzione, il file di markup deve essere compilato in un file di risorse in formato binario. Un compilatore di markup della barra multifunzione dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso con Microsoft Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo. Oltre a compilare la versione binaria del markup della barra multifunzione, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.

[Migrazione al framework della barra multifunzione di Windows](ribbon-migration.md)

È possibile eseguire la migrazione di un'applicazione che si basa sui menu tradizionali, sulle barre degli strumenti e sulle finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi del Framework della barra multifunzione. Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle relative funzionalità.

[Informazioni sui comandi e sui controlli](windowsribbon-commandscontrols.md)

La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi del Framework della barra multifunzione, un sistema basato su uno schema progettuale in cui funzionalità e comportamento vengono implementate indipendentemente dai controlli che espongono questa funzionalità.

## <a name="user-interface"></a>Interfaccia utente

[Specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md)

Poiché è un sistema di presentazione dei comandi avanzato, il Framework della barra multifunzione è progettato per supportare ampiamente le risorse dell'immagine nell'interfaccia utente della barra multifunzione. Tutte le risorse immagine sono dichiarate in [markup della barra multifunzione](windowsribbon-schema.md) o eseguite da un'applicazione host della barra multifunzione.

Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.

[Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md)

I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.

[Uso delle raccolte](ribbon-controls-galleries.md)

Il Framework della barra multifunzione offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati sulle raccolte. Grazie all'adattamento e alla riconfigurazione dell'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al Framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione e offrono la flessibilità necessaria per gestire diversi ambienti di Runtime.

[Visualizzazione di schede contestuali](ribbon-contextualtabs.md)

In un'applicazione Ribbon Framework, una scheda contestuale è un controllo struttura a [schede](windowsribbon-controls-tab.md) nascosto visualizzato nella scheda quando un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine, viene selezionato o evidenziato.

[Riconfigurazione della barra multifunzione con le modalità applicazione](ribbon-applicationmodes.md)

Il Framework della barra multifunzione supporta la riconfigurazione dinamica e l'esposizione degli elementi principali dell'interfaccia utente della barra multifunzione in fase di esecuzione, in base allo stato dell'applicazione (noto anche come contesto). Dichiarati e associati a elementi specifici nel markup, i vari stati supportati da un'applicazione sono definiti modalità applicazione.

[Personalizzazione dei colori della barra multifunzione](ribbon-color.md)

Il Framework della barra multifunzione espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di diversi elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.

[Visualizzazione della barra multifunzione](ribbon-visibility.md)

Il Framework della barra multifunzione espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.

## <a name="management"></a>Gestione

[Mantenimento dello stato della barra multifunzione](ribbon-statepersistence.md)

Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.

[Ascolto degli eventi della barra multifunzione](listening-for-ribbon-events.md)

Il Framework della barra multifunzione usa l'infrastruttura di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.

## <a name="markup-compiler"></a>Compilatore di markup

[Compilazione del markup della barra multifunzione](windowsribbon-intentcl.md)

Affinché il Framework della barra multifunzione utilizzi il file di [markup della barra multifunzione](windowsribbon-schema.md) , il file di markup deve essere compilato in un file di risorse in formato binario. Un compilatore di markup dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso con Microsoft Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo. Oltre a compilare la versione binaria del markup, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.

[Informazioni sui messaggi del compilatore di markup](windowsribbon-compilationerrors.md)

Il compilatore di markup di Windows Ribbon Framework (barra multifunzione), il compilatore di comandi dell'interfaccia utente (UICC.exe), convalida il markup della barra multifunzione rispetto allo schema della barra multifunzione e un set aggiuntivo di regole definito dal framework della barra multifunzione.

 

 