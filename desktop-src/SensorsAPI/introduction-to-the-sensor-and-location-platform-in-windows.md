---
description: Il sistema operativo Windows 7 offre supporto incorporato per i dispositivi dei sensori.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Panoramica della piattaforma sensore e posizione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01b6d3132ad6e1bc299895bc39668edbe19b91c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966576"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Panoramica della piattaforma sensore e posizione di Windows

Il sistema operativo Windows 7 offre supporto incorporato per i dispositivi dei sensori. Questo include il supporto per i sensori di posizione, ad esempio i dispositivi GPS. Come parte di questo supporto, la piattaforma sensore e posizione di Windows offre agli sviluppatori di software un modo standard per esporre i dispositivi sensori agli sviluppatori e ai consumer. Allo stesso tempo, la piattaforma offre agli sviluppatori un'API standardizzata e un'interfaccia di driver di dispositivo (DDI) per lavorare con i sensori e i dati del sensore.

## <a name="about-sensor-devices"></a>Informazioni sui dispositivi sensori

I sensori sono disponibili in molte configurazioni e, da una certa prospettiva, qualsiasi elemento che fornisce dati sui fenomeni fisici può essere definito sensore. Sebbene i sensori siano in genere considerati come dispositivi hardware, i sensori logici possono anche fornire informazioni tramite l'emulazione della funzionalità dei sensori nel software o nel firmware. Inoltre, un singolo dispositivo hardware può contenere più sensori.

La piattaforma sensore e posizione di Windows organizza i sensori in *categorie*, che rappresentano classi generali di dispositivi sensori e *tipi*, che rappresentano tipi specifici di sensori. Ad esempio, un sensore in un controller di gioco video che rileva la posizione e lo spostamento della mano di un giocatore, ad esempio per un gioco di bowling video, verrebbe categorizzato come un sensore di orientamento, ma il relativo tipo sarebbe un accelerometro 3D. Nel codice, Windows rappresenta le categorie e i tipi usando identificatori univoci globali (GUID), molti dei quali sono predefiniti. I produttori di dispositivi possono creare nuove categorie e tipi definendo e pubblicando i nuovi GUID, quando necessario.

I dispositivi di posizione costituiscono una categoria particolarmente interessante. A questo punto, la maggior parte degli utenti ha familiarità con i sistemi di posizionamento globale (GPS). In Windows un sensore GPS fa parte della categoria location. La categoria location può includere altri tipi di sensori. Alcuni di questi tipi di sensori sono basati su software, ad esempio un resolver IP che fornisce informazioni sulla posizione basate su un indirizzo Internet, un triangolare della torre mobile phone che determina la posizione in base alle torri vicine o un provider del percorso di rete Wi-Fi che legge le informazioni sulla posizione dall'hub di rete wireless connesso.

## <a name="about-the-platform"></a>Informazioni sulla piattaforma

La piattaforma sensore e posizione di Windows è costituita dai seguenti componenti per sviluppatori e utenti:

-   L'interfaccia DDI consente a Windows di fornire un modo standard per i dispositivi sensori di connettersi al computer e fornire dati ad altri sottosistemi.
-   L'API del sensore di Windows fornisce un set di metodi, proprietà ed eventi da usare con i sensori e i dati dei sensori connessi.
-   L'API location di Windows, basata sull'API del sensore Windows, fornisce un set di oggetti di programmazione, inclusi gli oggetti di script, per l'utilizzo delle informazioni sulla posizione.
-   Il pannello di controllo posizione e altri sensori consente agli amministratori dei computer di impostare i sensori, inclusi i sensori di posizione, per ogni utente.

Le sezioni seguenti descrivono ognuno di questi componenti.

## <a name="architecture-diagram"></a>Diagramma dell'architettura

Nel diagramma seguente viene illustrata la relazione tra i componenti.

![diagramma della piattaforma del sensore e della posizione](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interfaccia del driver di dispositivo

I produttori di sensori possono creare driver di dispositivo per connettere i sensori con Windows 7. I driver di dispositivo del sensore vengono implementati utilizzando il modello di driver dispositivi portatili Windows (WPD), basato sul Framework driver in modalità utente di Windows (UMDF). Molti driver di dispositivo sono stati scritti usando questi Framework. Poiché queste tecnologie vengono stabilite, i programmatori di driver di dispositivo esperti troveranno la scrittura di un driver del sensore come attività familiare. Il sensore DDI usa tipi di dati e interfacce UMDF e WPD specifici e definisce anche i comandi e i parametri di WPD specifici del sensore, dove è necessario. Per ulteriori informazioni sulla creazione di driver di dispositivo sensore, vedere Windows Driver Kit.

## <a name="sensor-api"></a>API Sensor

L'API del sensore consente agli sviluppatori C++ di creare programmi basati sui sensori usando un set di interfacce COM. L'API definisce le interfacce per eseguire attività comuni di programmazione dei sensori che includono la gestione dei sensori per categoria, tipo o ID, la gestione degli eventi dei sensori, l'uso di singoli sensori e raccolte di sensori e l'uso dei dati del sensore. Il Windows SDK include file di intestazione, documentazione, esempi e strumenti che consentono agli sviluppatori di software di utilizzare i sensori nei programmi Windows. Questa documentazione descrive l'API del sensore.

## <a name="location-api"></a>API location

Basato sull'API dei sensori, l'API Location fornisce un modo semplice per recuperare dati sulla posizione geografica proteggendo al tempo stesso la privacy degli utenti. L'API Location fornisce le funzionalità tramite un set di interfacce COM che rappresentano oggetti. Questi oggetti possono essere usati dai programmatori che sanno come usare COM tramite il linguaggio di programmazione C++ o in linguaggi di scripting, ad esempio JScript. Il supporto per gli script consente di accedere facilmente ai dati del percorso per i progetti eseguiti nell'area del computer locale, ad esempio i gadget. Il Windows SDK include file di intestazione, documentazione (inclusa la documentazione di riferimento per gli script), esempi e strumenti per aiutare gli sviluppatori Web e software a utilizzare le informazioni sulla posizione nei programmi.

## <a name="location-and-other-sensors-control-panel"></a>Pannello di controllo posizione e altri sensori

Windows 7 include un pannello di controllo che consente agli amministratori di computer di abilitare o disabilitare i sensori a livello di sistema o per ogni utente. Poiché alcuni sensori possono esporre dati sensibili, questa interfaccia utente consente agli amministratori di controllare se tutti i programmi hanno accesso a ogni sensore per ogni utente. Gli utenti possono anche visualizzare le proprietà dei sensori e modificare la descrizione del sensore visualizzata nell'interfaccia utente.

Il pannello di controllo fornisce anche una pagina di percorso predefinita per consentire agli utenti di fornire il proprio percorso. Quando non è disponibile alcun sensore, la piattaforma utilizzerà il percorso fornito dall'utente. Gli utenti possono specificare campi di indirizzi civici che includono via, città, stato o provincia e paese o area geografica.

## <a name="related-topics"></a>Argomenti correlati

[Informazioni sull'API del sensore](about-the-sensor-api.md)

[Sito Web Windows Hardware Developer Central](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Windows Dev Center](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
