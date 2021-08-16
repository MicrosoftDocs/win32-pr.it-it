---
title: Informazioni su Direct2D
description: Introduce Direct2D, un'API che offre agli sviluppatori Win32 la possibilità di eseguire attività di rendering della grafica 2D con prestazioni e qualità visiva superiori.
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
ms.openlocfilehash: fbe011b2d61fbb116efa4818f0db988d24e39fcb707e3ae42ddc0fb91f065652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825584"
---
# <a name="about-direct2d"></a>Informazioni su Direct2D

Questo argomento presenta Direct2D, un'API che offre agli sviluppatori Win32 la possibilità di eseguire attività di rendering della grafica 2D con prestazioni e qualità visiva superiori.

## <a name="what-is-direct2d"></a>Che cos'è Direct2D?

Direct2D è un'API grafica 2D con accelerazione hardware e in modalità immediata che offre prestazioni elevate e rendering di alta qualità per geometria 2D, bitmap e testo. L'API Direct2D è progettata per interagire con il codice esistente che usa GDI, GDI+ o Direct3D.

Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:

-   Sviluppatori di applicazioni native di grandi dimensioni su scala aziendale.
-   Sviluppatori che creano toolkit e librerie di controllo per l'utilizzo da parte degli sviluppatori downstream.
-   Sviluppatori che richiedono il rendering lato server di grafica 2D.
-   Sviluppatori che usano grafica Direct3D e necessitano di rendering 2D e testo semplice e ad alte prestazioni per menu, elementi dell'interfaccia utente e hud(HUD).

## <a name="why-direct2d"></a>Perché Direct2D?

Le motivazioni principali per la creazione di una nuova API grafica 2D in Microsoft Windows includono quanto segue:

-   Per tenere il passo con l'aumento del livello di Windows a cui sono abituati gli utenti.
-   Per consentire agli sviluppatori di scrivere codice di rendering 2D che viene ridimensionato direttamente con l'hardware di elaborazione grafica del PC in cui è in esecuzione.
-   Per consentire agli sviluppatori di scrivere codice per il rendering di grafica 2D che può essere eseguito nel contesto di un servizio.

Negli ultimi anni, gli utenti finali hanno iniziato a aspettarsi una maggiore fedeltà visiva nelle esperienze digitali. Questa tendenza si riflette nell'elettronica di consumo. I dispositivi GPS, i dispositivi di riproduzione multimediale, i telefoni cellulari e le fotocamere digitali offrono esperienze costantemente più arricchite anno dopo anno. Questa tendenza può essere osservata anche nella diversità del contenuto grafico in film, tv, videogiochi e sul Web. Per tenere il passo con queste modifiche, agli sviluppatori viene chiesto in modo coerente di portare le applicazioni Windows esistenti al livello successivo di arricchizione visiva.

Anche i processori di grafica nei PC Windows moderni sono in continua evoluzione, grazie ai progressi nella grafica dei videogiochi e in parti dell'esperienza Windows come Windows Media Center e Aero. Alcune Windows applicazioni possono sfruttare i vantaggi delle GPU moderne usando Microsoft Direct3D e Windows Presentation Foundation (WPF). Mentre Direct3D serve applicazioni grafiche 3D di fascia alta e WPF risolve le esigenze degli sviluppatori .NET, esistono lacune per gli sviluppatori che hanno codebase di codice di rendering esistenti di grandi dimensioni basate su GDI e GDI+ o che vogliono incorporare grafica 2D di alta qualità nelle applicazioni basate su Direct3D.

Infine, la necessità di un'API grafica che può essere usata in un servizio è diventata un requisito emergente per gli sviluppatori che lavorano in scenari aziendali e di sviluppo Web. Le API di rendering esistenti sono incentrate sul rendering lato client in una singola sessione utente. Di conseguenza, possono essere poco efficaci in aree di affidabilità e scalabilità quando vengono usate in un contesto del servizio. Per risolvere questo problema, è necessaria una nuova API.

## <a name="high-performance-with-maximum-availability"></a>Prestazioni elevate con disponibilità massima

Direct2D è una libreria in modalità utente creata usando l'API Direct3D 10.1. Ciò significa che le applicazioni Direct2D traggono vantaggio dal rendering con accelerazione hardware nelle MODERNE GPU Mainstream. L'accelerazione hardware viene ottenuta anche nell'hardware Direct3D 9 precedente usando il rendering Direct3D 10-level-9. Questa combinazione offre prestazioni eccellenti sull'hardware grafico nei PC Windows esistenti.

> [!Note]  
> A partire Windows 8, Direct2D viene compilato usando l'API Direct3D 11.1.

 

Il diagramma seguente illustra l'architettura a più livelli di Direct2D.

![Diagramma dell'architettura a più livelli direct2d](images/direct2d-architectual-layering.png)

Per gli scenari in cui l'uso dell'accelerazione hardware non è fattibile, Direct2D include un rasterizzatore software ad alte prestazioni. Quando si esegue il rendering nel software, le applicazioni che usano Direct2D hanno prestazioni di rendering notevolmente migliori rispetto GDI+ e con qualità visiva simile. L'rasterizzazione software è progettata anche per l'uso in un contesto del servizio.

Il contenuto di cui viene eseguito il rendering tramite Direct2D può anche essere visualizzato in remoto usando l'infrastruttura Remote Desktop Protocol (RDP) nel sistema operativo Windows 7. Gli sviluppatori possono scegliere se il rendering viene gestito dalla GPU nel computer di visualizzazione o in locale e trasmesso come bitmap. Questa scelta può essere effettuata in base alla velocità di riempimento richiesta e alla quantità di primitive grafiche di cui viene eseguito il rendering. Quando il computer di visualizzazione esegue un sistema operativo precedente a Windows 7, il rendering dello schermo remoto viene eseguito trasmettendo bitmap in rete.

Fornendo una singola API che combina le prestazioni di Direct3D e la disponibilità elevata fornendo fallback software, desktop remoto e rendering del servizio, Direct2D consente agli sviluppatori di avere una singola implementazione per il rendering ad alte prestazioni in molti scenari diversi.

## <a name="visual-quality"></a>Qualità visiva

Le applicazioni che usano Direct2D per la grafica possono offrire una qualità visiva superiore rispetto a ciò che è possibile ottenere con GDI. Direct2D usa l'antialiasing per primitivo per offrire curve e linee dall'aspetto più uniformi nel contenuto sottoposto a rendering. È inoltre disponibile il supporto completo per la trasparenza e la fusione alfa durante il rendering di primitive 2D. Le immagini seguenti confrontano il contenuto con alias di cui viene eseguito il rendering usando GDI (a sinistra) con il contenuto con antialias sottoposto a rendering da Direct2D (a destra).

![illustrazione di curve e linee di cui viene eseguito il rendering in gdi e in direct2d](images/rendering-curves-and-lines.png)

Gli sviluppatori possono specificare il rendering con alias della grafica vettoriale. Viene usato negli scenari in cui è necessario l'allineamento ai limiti dei pixel rigidi, ad esempio elementi dell'interfaccia utente come puntatori o righelli, se è necessario associare lo stile GDI di output o se l'antialiasing verrà eseguito a valle nel processo di rendering tramite l'anti-aliasing multisample o un altro meccanismo.

## <a name="interoperability"></a>Interoperabilità

L'integrazione del rendering basato su Direct2D è semplificata per gli sviluppatori grazie all'interoperabilità a livello di superficie con GDI e Direct3D. Le applicazioni che eseguono il rendering del contenuto principalmente con GDI, GDI+ o Direct3D possono iniziare usando Direct2D per eseguire il rendering di aree specifiche dell'applicazione e nel tempo passare a un modello in cui il rendering viene eseguito principalmente tramite Direct2D, usando GDI principalmente per plug-in o estendibilità legacy.

Direct2D semplifica anche l'uso [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) testo di alta qualità e le funzionalità avanzate di creazione dell'immagine di [Microsoft Windows Imaging Component (WIC).](https://msdn.microsoft.com/library/ms737408.aspx)

Per altre informazioni sull'interoperabilità Direct2D, vedere la [sezione Interoperabilità di Direct2D SDK.](interoperability.md)

## <a name="summary"></a>Riepilogo

Microsoft Direct2D consente agli sviluppatori di creare funzionalità grafiche 2D nelle proprie applicazioni che offrono una migliore qualità visiva rispetto a GDI e caratteristiche di prestazioni scalabili con GPU moderne. Il modello di interoperabilità Direct2D consente agli sviluppatori di eseguire la migrazione selettiva di parti dell'applicazione alla volta insieme al rendering basato su GDI, GDI+ o Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida introduttiva di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Panoramica dell'API Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 