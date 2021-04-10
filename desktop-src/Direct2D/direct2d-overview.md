---
title: Informazioni su Direct2D
description: Introduce Direct2D, un'API che fornisce agli sviluppatori Win32 la possibilità di eseguire attività di rendering grafiche 2D con prestazioni e qualità visive superiori.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, informazioni
- Direct2D, interoperabilità
- Direct2D, prestazioni
- Direct2D, disponibilità
- Direct2D, applicazioni
- interoperabilità, Direct2D
- prestazioni per Direct2D
- disponibilità per Direct2D
- applicazioni per Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963286"
---
# <a name="about-direct2d"></a>Informazioni su Direct2D

In questo argomento viene presentata la funzionalità Direct2D, un'API che consente agli sviluppatori Win32 di eseguire attività di rendering di grafica 2D con prestazioni e qualità visive superiori.

## <a name="what-is-direct2d"></a>Che cos'è Direct2D?

Direct2D è un'API grafica 2D in modalità immediata e con accelerazione hardware che fornisce prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo. L'API Direct2D è progettata per interagire con il codice esistente che usa GDI, GDI+ o Direct3D.

Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:

-   Sviluppatori di applicazioni native di grandi dimensioni e di livello aziendale.
-   Sviluppatori che creano Toolkit e librerie di controllo per l'uso da parte degli sviluppatori downstream.
-   Sviluppatori che richiedono il rendering lato server della grafica 2D.
-   Gli sviluppatori che utilizzano la grafica Direct3D e necessitano di rendering semplice e a prestazioni elevate 2D e di testo per menu, elementi dell'interfaccia utente e visualizzazioni Heads-up (HUDs).

## <a name="why-direct2d"></a>Perché Direct2D?

Le motivazioni principali per la creazione di una nuova API grafica 2D in Microsoft Windows sono le seguenti:

-   Per restare al passo con l'aumento del livello di ricchezza visiva a cui gli utenti di Windows sono abituati.
-   Per consentire agli sviluppatori di scrivere codice di rendering 2D scalabile direttamente con l'hardware di elaborazione grafica del PC in cui è in esecuzione.
-   Per consentire agli sviluppatori di scrivere codice per il rendering di immagini 2D che possono essere eseguite nel contesto di un servizio.

Negli ultimi anni, gli utenti finali hanno iniziato a aspettarsi una maggiore fedeltà visiva nelle esperienze digitali. Questa tendenza si riflette nell'elettronica consumer. I dispositivi GPS, i dispositivi di riproduzione multimediale, i telefoni cellulari e le fotocamere digitali offrono esperienze costantemente più ricche di anno dopo anno. Questa tendenza può essere considerata anche nella diversità di contenuti grafici in film, televisori, giochi video e sul Web. Per rimanere al passo con queste modifiche, gli sviluppatori vengono costantemente invitati a portare le proprie applicazioni Windows esistenti al livello successivo di ricchezza visiva.

I processori grafici nei PC Windows moderni si sono evoluti costantemente, grazie ai miglioramenti apportati alla grafica dei giochi video e alle parti dell'esperienza Windows come Windows Media Center e Aero. Alcune applicazioni Windows possono sfruttare le GPU moderne usando Microsoft Direct3D e Windows Presentation Foundation (WPF). Sebbene Direct3D soddisfi le applicazioni grafiche 3D di fascia alta e WPF soddisfi le esigenze degli sviluppatori .NET, esistono Gap per gli sviluppatori che dispongono di codebase esistenti di grandi dimensioni per il rendering del codice basato su GDI e GDI+ o che desiderano incorporare grafica 2D di alta qualità nelle applicazioni basate su Direct3D.

Infine, la necessità di un'API grafica che può essere usata in un servizio è diventata un requisito emergente per gli sviluppatori che lavorano in scenari aziendali e di sviluppo Web. Le API di rendering esistenti si concentrano sul rendering lato client in una singola sessione utente. Di conseguenza, possono essere suddivisi in aree di solidità e scalabilità quando vengono usati in un contesto del servizio. Per risolvere il problema, è necessaria una nuova API.

## <a name="high-performance-with-maximum-availability"></a>Prestazioni elevate con disponibilità massima

Direct2D è una libreria in modalità utente compilata con l'API Direct3D 10,1. Ciò significa che le applicazioni Direct2D traggono vantaggio dal rendering con accelerazione hardware sulle GPU mainstream moderne. L'accelerazione hardware viene inoltre realizzata nell'hardware precedente di Direct3D 9 usando il rendering Direct3D 10-Level-9. Questa combinazione fornisce prestazioni ottimali per l'hardware grafico nei PC Windows esistenti.

> [!Note]  
> A partire da Windows 8, Direct2D viene creato usando l'API Direct3D 11,1.

 

Il diagramma seguente mostra l'architettura a più livelli di Direct2D.

![diagramma dell'architettura a più livelli Direct2D](images/direct2d-architectual-layering.png)

Per gli scenari in cui l'utilizzo dell'accelerazione hardware non è fattibile, Direct2D include un rasterizzatore software a prestazioni elevate. Quando si esegue il rendering nel software, le applicazioni che utilizzano Direct2D presentano prestazioni notevolmente migliori rispetto a GDI+ e con una qualità visiva simile. L'rasterizzatore software è inoltre progettato per essere utilizzato in un contesto del servizio.

Il contenuto di cui è stato eseguito il rendering tramite Direct2D può essere visualizzato anche in modalità remota tramite l'infrastruttura di Remote Desktop Protocol (RDP) nel sistema operativo Windows 7. Gli sviluppatori possono scegliere se il rendering viene gestito dalla GPU nel computer di visualizzazione o sottoposto a rendering localmente e trasmesso come bitmap. Questa scelta può essere eseguita in base alla velocità di riempimento richiesta e alla quantità di primitive di grafica di cui viene eseguito il rendering. Quando il computer di visualizzazione esegue un sistema operativo precedente a Windows 7, il rendering della visualizzazione remota viene eseguito trasmettendo le bitmap sulla rete.

Grazie a una singola API che combina le prestazioni di Direct3D e disponibilità elevata grazie al fallback software, al desktop remoto e al rendering del servizio, Direct2D consente agli sviluppatori di disporre di una singola implementazione per il rendering ad alte prestazioni in molti scenari diversi.

## <a name="visual-quality"></a>Qualità visiva

Le applicazioni che utilizzano Direct2D per la grafica possono fornire una qualità visiva superiore rispetto a quella che è possibile ottenere utilizzando GDI. Direct2D usa l'anti-aliasing per primitive per offrire curve e linee più semplici e in contenuto renderizzato. Quando si esegue il rendering di primitive 2D, è inoltre disponibile il supporto completo per la trasparenza e la fusione alfa. Le immagini seguenti confrontano il contenuto con alias con il rendering tramite GDI (a sinistra) con contenuto con antialias di cui è stato eseguito il rendering da Direct2D (sulla destra).

![illustrazione delle curve e delle linee di cui viene eseguito il rendering in GDI e in Direct2D](images/rendering-curves-and-lines.png)

Gli sviluppatori possono specificare il rendering con alias di grafica vettoriale. Viene usato in scenari in cui è necessario l'allineamento a limiti di pixel reali, ad esempio elementi dell'interfaccia utente come puntatori o righelli, se è necessario trovare una corrispondenza per lo stile GDI dell'output o se l'anti-aliasing verrà eseguito a valle nel processo di rendering tramite l'anti-aliasing multicampionamento o un altro meccanismo.

## <a name="interoperability"></a>Interoperabilità

L'integrazione del rendering basato su Direct2D è semplificata per gli sviluppatori grazie all'interoperabilità a livello di superficie con GDI e Direct3D. Le applicazioni che eseguono il rendering del contenuto principalmente con GDI, GDI+ o Direct3D possono iniziare utilizzando Direct2D per eseguire il rendering di aree specifiche dell'applicazione e nel tempo passare a un modello in cui il rendering viene eseguito principalmente tramite Direct2D, usando GDI principalmente per i plug-in o l'estendibilità legacy.

Direct2D semplifica inoltre l'utilizzo di [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) per il testo di alta qualità e le funzionalità avanzate di creazione di immagini di [Microsoft Windows Imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).

Per ulteriori informazioni sull'interoperabilità Direct2D, vedere la [sezione interoperabilità di DIRECT2D SDK.](interoperability.md)

## <a name="summary"></a>Riepilogo

Microsoft Direct2D consente agli sviluppatori di creare funzionalità grafiche 2D nelle applicazioni che offrono una migliore qualità visiva rispetto a GDI e caratteristiche di prestazioni che si adattano alle GPU moderne. Il modello di interoperabilità Direct2D consente agli sviluppatori di eseguire la migrazione selettiva di parti dell'applicazione contemporaneamente insieme a GDI, GDI+ o al rendering basato su Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida introduttiva di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Panoramica dell'API Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 