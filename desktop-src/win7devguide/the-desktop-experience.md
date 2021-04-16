---
title: Esperienza desktop
description: Il nuovo desktop di Windows 7 consente di portare le proprie applicazioni alla vita.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3476f70c46aecceb365e17dba1803b876fd51e8d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104550149"
---
# <a name="the-desktop-experience"></a>Esperienza desktop

Il nuovo desktop di Windows 7 consente di portare le proprie applicazioni alla vita. Le applicazioni sono ora più individuabili, informative e interattive. Le interfacce utente moderne e intuitive sono più facili da sviluppare con Windows 7. Le nuove esperienze per desktop e applicazioni includono quanto segue:

-   La barra delle applicazioni avanzata introduce anteprime interattive e Abilita l'animazione e l'interazione per le applicazioni ridotte a icona.
-   Il concetto di destinazioni consente agli utenti di passare con un solo clic ai file, alle posizioni o alle attività che usano più di frequente.
-   Sono disponibili nuovi controlli e API per la *barra multifunzione*, basati sull'interfaccia utente di Office Fluent, per aggiungere facilmente controlli di tipo *Ribbon*, menu e raccolte alle applicazioni.
-   Un Framework di animazione consente di migliorare le animazioni personalizzate.

I miglioramenti apportati alla piattaforma Gadget consentono alle applicazioni di installare gadget complementari durante l'installazione o l'esperienza di prima esecuzione.

![Screenshot che mostra il desktop di Windows 7.](images/windows7-6.jpg)

Il nuovo desktop di Windows 7 consente di portare le proprie applicazioni alla vita

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Jump List: è possibile ottenere rapidamente gli utenti nell'applicazione

Le Jump List consentono agli utenti di spostarsi più velocemente. Le Jump List sono file, URL, attività o elementi personalizzati aperti all'interno dell'applicazione. Il menu nuovo Jump List nel menu *Start* e la barra delle applicazioni rendono disponibili le destinazioni comuni e le attività principali con un solo clic. Il menu Jump List viene popolato automaticamente in base alla frequenza e alla modalità di utilizzo degli elementi di recente. Gli sviluppatori possono fornire Jump List personalizzati in base alla propria semantica. Le applicazioni possono anche definire le *attività* da visualizzare nei propri menu, ovvero azioni dell'applicazione a cui gli utenti vogliono accedere direttamente, ad esempio la composizione di un messaggio di posta elettronica. Vedere [estensioni della barra delle applicazioni](../shell/taskbar-extensions.md) e [interfaccia ICustomDestinationList](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist).

![Jump List](images/windows7-7.jpg)

Le Jump List consentono agli utenti di spostarsi più velocemente

## <a name="enhanced-taskbar"></a>Barra delle applicazioni avanzata

Grazie alla nuova barra delle applicazioni di Windows 7, le applicazioni possono fornire più informazioni all'utente in modo più intuitivo. Ad esempio, le applicazioni possono visualizzare le barre di avanzamento nei pulsanti della barra delle applicazioni, in modo che gli utenti possano restare a conoscenza dello stato di avanzamento senza dover mantenere visibile la finestra. Questa operazione è utile per tenere traccia di operazioni che richiedono molto tempo, come la copia di file, i download, le installazioni o la masterizzazione di contenuti multimediali. Le sovrimpressioni delle icone possono essere visualizzate nell'area inferiore destra del pulsante della barra delle applicazioni dell'applicazione e vengono usate per comunicare lo stato o le notifiche (ad esempio, la nuova posta elettronica). Le nuove API di anteprima consentono a un'applicazione di definire le finestre figlio e le immagini di anteprima corrispondenti per tali finestre. La barra degli strumenti dell'anteprima consente di controllare le azioni comuni senza richiedere il ripristino della finestra, ad esempio *Play/Stop* per i supporti. (Vedere [estensioni della barra delle applicazioni](../shell/taskbar-extensions.md) e [Windows 7: risorse per sviluppatori](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples)).

## <a name="gadgets-platform"></a>Piattaforma Gadget

I gadget sono una funzionalità comune del desktop di Windows Vista e in Windows 7 è ancora più semplice per le applicazioni installare i gadget. In Windows 7, un'applicazione può aggiungere a livello di codice un gadget al desktop di Windows durante l'installazione dell'applicazione o la prima esecuzione. Ciò significa che un'applicazione predefinita può includere una semplice casella di controllo, ad esempio, per installare un gadget complementare disponibile sul desktop non appena l'applicazione è pronta per essere usata. Vedere [Introduzione alla piattaforma Gadget](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform).

![Gadget di Windows](images/windows7-8.jpg)

In Windows 7, è ancora più semplice per le applicazioni installare i gadget

## <a name="windows-ribbon"></a>Barra multifunzione di Windows



Il controllo della barra multifunzione di Windows consente agli sviluppatori di migliorare l'usabilità esponendo le funzionalità di accesso più frequente dell'applicazione direttamente agli utenti finali. La barra multifunzione rende più semplice per gli utenti finali trovare e usare le funzionalità dell'applicazione, perché una minore funzionalità è nascosta, ottenendo una maggiore produttività. La barra multifunzione è progettata come alternativa basata su finalità al modello di presentazione dei comandi di menu, barre degli strumenti, riquadri attività e finestre di dialogo in applicazioni standard basate su Windows.

I controlli della barra multifunzione sono costituiti da un set di Win32APIs che eseguono l'override della funzionalità della barra dei menu di primo livello ed eseguono il rendering di un'interfaccia utente del comando di tipo Ribbon È simile a funzionalità e aspetto alla *barra multifunzione* di Office System 2007. L'interfaccia utente è costituita da diversi controlli secondari che includono gli elementi seguenti:

-   Pulsante applicazione (o perla)
-   Barra di accesso rapido
-   Controllo *Ribbon* di schede contestuali
-   Barre degli strumenti mini
-   Raccolte di stili

I modelli e la creazione di markup sono disponibili per gli sviluppatori per lo sviluppo e l'integrazione rapidi delle funzionalità della barra multifunzione. (Vedere [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md) e [Windows Ribbon Framework: risorse per sviluppatori](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon)).

![barra degli strumenti barra multifunzione](images/windows7-9.jpg)

Il controllo Ribbon consente agli sviluppatori di migliorare l'usabilità esponendo le funzionalità di cui si accede più di frequente.

## <a name="animation"></a>Animazione

Le animazioni Smooth sono fondamentali per molte applicazioni dell'interfaccia utente grafica e Windows 7 introduce un Framework di animazione nativo per la gestione della pianificazione e dell'esecuzione di animazioni. Il Framework di animazione fornisce una libreria di funzioni matematiche utili per specificare il comportamento nel tempo e consente inoltre agli sviluppatori di fornire le proprie funzioni di comportamento. Il Framework supporta una risoluzione sofisticata dei conflitti quando più animazioni tentano di modificare lo stesso valore nello stesso momento. Un'applicazione può specificare che un'animazione deve essere completata prima che un altro possa essere avviato e possa forzare il completamento entro un periodo di tempo impostato. Il nuovo Framework aiuta anche le animazioni a determinare le durate appropriate. (Vedere [Windows Animation Manager](../uianimation/-main-portal.md)).

 

 