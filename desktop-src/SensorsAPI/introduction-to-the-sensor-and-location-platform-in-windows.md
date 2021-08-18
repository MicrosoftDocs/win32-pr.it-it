---
description: Il Windows 7 offre il supporto incorporato per i dispositivi sensore.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Panoramica del sensore Windows e della piattaforma di posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4847d6d6137b91ce577cfce0dbc54cc8c6e19430e1318eaff145c24ce493af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889731"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Panoramica del sensore Windows e della piattaforma di posizione

Il Windows 7 offre il supporto incorporato per i dispositivi sensore. Ciò include il supporto per i sensori di posizione, ad esempio i dispositivi GPS. Come parte di questo supporto, la piattaforma Windows Sensor and Location offre ai produttori di dispositivi un modo standard per esporre i dispositivi dei sensori agli sviluppatori di software e agli utenti. Allo stesso tempo, la piattaforma offre agli sviluppatori un'API standardizzata e un'interfaccia DDI (Device Driver Interface) per lavorare con sensori e dati dei sensori.

## <a name="about-sensor-devices"></a>Informazioni sui dispositivi dei sensori

I sensori sono disponibili in molte configurazioni e, da un certo punto di vista, quasi tutto ciò che fornisce dati sui fenomenali fisici può essere chiamato sensore. Anche se in genere si pensa ai sensori come dispositivi hardware, i sensori logici possono anche fornire informazioni tramite l'emulazione delle funzionalità dei sensori nel software o nel firmware. Inoltre, un singolo dispositivo hardware può contenere più sensori.

La Windows Sensor e Location organizza i sensori in categorie *,* che rappresentano ampie classi di dispositivi sensore e tipi *,* che rappresentano tipi specifici di sensori. Ad esempio, un sensore in un controller di videogiochi che rileva la posizione e lo spostamento della mano di un giocatore (ad esempio per un gioco di bowling video) verrebbe classificato come sensore di orientamento, ma il suo tipo sarebbe accelerometro 3D. Nel codice, Windows categorie e tipi usando identificatori univoci globali (GUID), molti dei quali sono predefiniti. I produttori di dispositivi possono creare nuove categorie e tipi definendo e pubblicando nuovi GUID, quando necessario.

I dispositivi di posizione costituiscono una categoria particolarmente interessante. A questo punto, la maggior parte delle persone ha familiarità con i sistemi di posizionamento globale (GPS). In Windows, un sensore GPS fa parte della categoria Posizione. La categoria Posizione può includere altri tipi di sensore. Alcuni di questi tipi di sensori sono basati su software, ad esempio un sistema di risoluzione IP che fornisce informazioni sulla posizione in base a un indirizzo Internet, un dispositivo mobile tower triangolator che determina la posizione in base alle torri vicine o un provider di posizione di rete Wi-Fi che legge le informazioni sulla posizione dall'hub di rete wireless connesso.

## <a name="about-the-platform"></a>Informazioni sulla piattaforma

La Windows Sensor and Location è costituita dai componenti per sviluppatori e utenti seguenti:

-   DDI consente Windows un modo standard per consentire ai dispositivi sensore di connettersi al computer e di fornire dati ad altri sottosistemi.
-   L Windows'API Sensor fornisce un set di metodi, proprietà ed eventi da usare con i sensori connessi e i dati dei sensori.
-   L'API Windows Location, che si basa sull'API sensore Windows, fornisce un set di oggetti di programmazione, inclusi gli oggetti di scripting, per l'uso delle informazioni sulla posizione.
-   Il Sensore di posizione e altri sensori Pannello di controllo consente agli amministratori di computer di impostare sensori, inclusi i sensori di posizione, per ogni utente.

Le sezioni seguenti descrivono ognuno di questi componenti.

## <a name="architecture-diagram"></a>Diagramma dell'architettura

Il diagramma seguente illustra la relazione tra i componenti.

![Diagramma della piattaforma sensore e posizione](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interfaccia del driver di dispositivo

I produttori di sensori possono creare driver di dispositivo per connettere i sensori Windows 7. I driver di dispositivo del sensore vengono implementati usando il modello di driver WPD (Portable Devices) di Windows, basato su Windows User Mode Driver Framework (UMDF). Molti driver di dispositivo sono stati scritti usando questi framework. Poiché queste tecnologie sono state stabilite, i programmatori esperti di driver di dispositivo troveranno la scrittura di un driver di sensore come attività familiare. Il sensore DDI usa interfacce e tipi di dati UMDF e WPD specifici e definisce anche i comandi e i parametri WPD specifici del sensore, dove è necessario. Per altre informazioni sulla creazione di driver di dispositivo del sensore, vedere il Windows Driver Kit.

## <a name="sensor-api"></a>API Sensor

L'API Sensor consente agli sviluppatori C++ di creare programmi basati su sensori usando un set di interfacce COM. L'API definisce le interfacce per eseguire attività comuni di programmazione dei sensori che includono la gestione dei sensori per categoria, tipo o ID, la gestione degli eventi dei sensori, l'uso di singoli sensori e raccolte di sensori e l'uso dei dati dei sensori. L Windows SDK include file di intestazione, documentazione, esempi e strumenti per aiutare gli sviluppatori software a usare i sensori nei Windows software. Questa documentazione descrive l'API Sensor.

## <a name="location-api"></a>API di posizione

Basato sull'API Sensor, l'API Location offre un modo semplice per recuperare i dati sulla posizione geografica, proteggendo al tempo stesso la privacy degli utenti. L'API Location fornisce le funzionalità tramite un set di interfacce COM che rappresentano oggetti. Questi oggetti possono essere usati dai programmatori che comprendono come usare COM tramite il linguaggio di programmazione C++ o nei linguaggi di scripting, ad esempio JScript. Il supporto per gli script consente di accedere facilmente ai dati di posizione per i progetti eseguiti nell'area Computer locale, ad esempio i dispositivi di protezione. L Windows SDK include file di intestazione, documentazione (inclusa la documentazione di riferimento sugli script), esempi e strumenti che consentono agli sviluppatori Web e software di usare le informazioni sulla posizione nei programmi.

## <a name="location-and-other-sensors-control-panel"></a>Sensore di posizione e altri sensori Pannello di controllo

Windows 7 include un pannello di controllo che consente agli amministratori di computer di abilitare o disabilitare i sensori a livello di sistema o per ogni utente. Poiché alcuni sensori possono esporre dati sensibili, questa interfaccia utente consente agli amministratori di controllare se tutti i programmi hanno accesso a ogni sensore per ogni utente. Gli utenti possono anche visualizzare le proprietà del sensore e modificare la descrizione del sensore visualizzata nell'interfaccia utente.

Il Pannello di controllo fornisce anche una pagina Percorso predefinito per consentire agli utenti di specificare la propria posizione. Quando non è disponibile alcun sensore, la piattaforma userà la posizione fornita dall'utente. Gli utenti possono fornire campi di indirizzo civico, che includono l'indirizzo, la città, lo stato o la provincia e il paese o l'area geografica.

## <a name="related-topics"></a>Argomenti correlati

[Informazioni sull'API Sensor](about-the-sensor-api.md)

[Windows Sito Web di Hardware Developer Central](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Windows Dev Center](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
