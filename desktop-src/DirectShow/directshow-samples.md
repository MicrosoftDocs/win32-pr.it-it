---
description: DirectShow Campioni
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Campioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87687905d53f91339202af2b08bffa79902e100d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467358"
---
# <a name="directshow-samples"></a>DirectShow Campioni

Gli DirectShow seguenti sono inclusi in [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx). Si trovano nel percorso \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

La tabella seguente elenca tutti gli esempi DirectShow disponibili in Windows SDK. Per istruzioni su come compilare gli esempi, vedere la documentazione fornita in Windows SDK.

Se è disponibile documentazione aggiuntiva per un esempio, la prima colonna di questa tabella è collegata ad essa.




| Esempio | Area | Descrizione | Dipendenze aggiuntive | 
|--------|------|-------------|-------------------------|
| <a href="directshow-base-classes.md">DirectShow Classi di base</a> | Libreria di classi di base | Classi C++ e funzioni di utilità progettate per l'implementazione DirectShow filtri. | 
| <a href="amcap-sample.md">Esempio AmCap</a> | Acquisizione | Applicazione di acquisizione video. | strmbase.lib | 
| <a href="dvapp-sample.md">Esempio di DVApp</a> | Acquisizione | Applicazione di acquisizione di video digitali (DV). | 
| <a href="playcap-sample.md">Esempio PlayCap</a> | Acquisizione | Applicazione di acquisizione semplice. | 
| <a href="dmo-demo-sample.md">DMO Esempio dimostrativo</a> | DMO | Flussi dati audio da un file WAV tramite un effetto audio DMO. | DirectX SDK | 
| Esempio di DVD | DVD | Illustra la riproduzione e la navigazione dei DVD di base, oltre a funzionalità avanzate come la gestione a livello di genitori, i segnalibri, la sincronizzazione dei comandi e dei dvd. | 
| <a href="inftee-filter-sample.md">Esempio di filtro InfTee</a> | Filtri, vari | Implementazione di esempio del <a href="infinite-pin-tee-filter.md">filtro Infinite Pin Tee.</a> | strmbase.lib | 
| <a href="metronome-filter-sample.md">Esempio di filtro metronome</a> | Filtri, vari | Illustra come implementare un clock di riferimento. | strmbase.lib | 
| <a href="psi-parser-filter-sample.md">Esempio di filtro del parser PSI</a> | Filtri, vari | Riceve le tabelle PSI (Program Specific Information) da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma. | strmbase.lib | 
| <a href="dump-filter-sample.md">Esempio di filtro dump</a> | Filtri, renderer | Scrive gli esempi multimediali ricevuti in un file di testo. | strmbase.lib | 
| Filtro SampVid | Filtri, renderer | Filtro del renderer video. | strmbase.lib | 
| <a href="scope-filter-sample.md">Esempio di filtro ambito</a> | Filtri, renderer | Visualizza i dati audio come forme d'onda. | strmbase.lib | 
| <a href="async-filter-sample.md">Esempio di filtro asincrono</a> | Filtri, origine | Filtro lettore di file che supporta il download progressivo. | strmbase.lib | 
| <a href="ball-filter-sample.md">Esempio di filtro palla</a> | Filtri, origine | Filtro di origine video che produce un'immagine di una palla che si rigonfia. | strmbase.lib | 
| <a href="push-source-filters-sample.md">Esempio di filtri origine push</a> | Filtri, origine | Filtri di origine che forniscono i dati seguenti come flusso video: una singola bitmap, un set di bitmap, una copia dell'immagine desktop corrente. | strmbase.lib | 
| <a href="synth-filter-sample.md">Esempio di filtro synth</a> | Filtri, origine | Filtro di origine che genera forme d'onda audio. Questo esempio illustra la creazione dinamica di grafi. | strmbase.lib | 
| <a href="ezrgb24-filter-sample.md">Esempio di filtro EZRGB24</a> | Filtri, trasformazione | Filtro di elaborazione delle immagini. | strmbase.lib | 
| <a href="gargle-filter-sample.md">Esempio di filtro Gargle</a> | Filtri, trasformazione | Filtro dell'effetto audio. | strmbase.lib | 
| <a href="wavdest-filter-sample.md">Esempio di filtro WavDest</a> | Filtri, trasformazione | Scrive un flusso audio in un file WAV. | strmbase.lib | 
| <a href="dmoenum-sample.md">Esempio DMOEnum</a> | Varie | Illustra come enumerare <a href="directx-media-objects.md">oggetti multimediali DirectX</a> (DMO). | 
| <a href="mapper-sample.md">Esempio di mapper</a> | Varie | Illustra come usare Filter <a href="filter-mapper.md">Mapper per</a> trovare i filtri nel Registro di sistema. | 
| Esempio SysEnum | Varie | Illustra l'uso di <a href="system-device-enumerator.md">System Device Enumerator</a> per enumerare dispositivi e filtri. | 
| <a href="cutscene-sample.md">Esempio di CutScene</a> | Riproduzione | Riproduce un file video in modalità schermo intero. | 
| Esempio di DDrawXCL | Riproduzione | Riproduce video in modalità schermo intero esclusiva DirectDraw, usando l'interfaccia <a href="overlay-mixer-filter.md"></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> nel filtro di Mixer sovrimpressione. | 
| Esempio di DShowPlayer | Riproduzione | Applicazione di riproduzione video. | 
| Esempio di EVRPlayer | Riproduzione | Illustra come usare il filtro DirectShow EVR.<blockquote>[!Note]<br />Richiede Windows Vista o versione successiva.</blockquote><br /><br /> Questo esempio è disponibile in Windows SDK per Windows Server 2008 o versione successiva.<br /> | strmbase.lib | 
| Esempio Texture3D9 | Riproduzione | Disegna video su una superficie di trama di Microsoft DirectX 9.0. | strmbase.lib, DirectX SDK | 
| <a href="ticker-sample.md">Esempio di Ticker</a> | VMR-9 | Usa VMR-9 per unire video e testo. | 
| Esempio di VMR9Allocator | VMR-9 | Implementa un allocatore-presenter personalizzato per VMR-9. | strmbase.lib | 
| Esempio di VMR9Compositor | VMR-9 | Implementa un mixer personalizzato per VMR-9. | 
| <a href="vmrplayer-sample.md">Esempio di VMRPlayer</a> | VMR-9 | Usa VMR-9 per unire uno o due video in esecuzione e un'immagine statica. | 
| Esempio di filigrana | VMR-9 | Unisce una bitmap statica a un video durante la riproduzione, usando VMR-9. | 
| <a href="windowless-sample.md">Esempio senza finestra</a> | VMR-9 | Illustra la modalità senza finestra in VMR-9. | 




 

## <a name="additional-dependencies"></a>Dipendenze aggiuntive

Alcuni esempi si collegano alla libreria DirectShow di classi base. Per compilare questi esempi, è prima necessario compilare la libreria di classi di base. Per altre informazioni, vedere Classi [DirectShow base.](directshow-base-classes.md) La libreria di classi di base è necessaria per tutti i filtri di esempio.

Alcuni esempi richiedono anche DirectX SDK, oltre a Windows SDK. Per compilare questi esempi, è necessario installare DirectX SDK e impostare la variabile di ambiente %DXSDK DIR% uguale al percorso \_ di installazione di DirectX SDK.

Molti esempi di DirectShow usano un set di intestazioni e file di origine comuni che si trovano in Directrory \[ SDK Root Samples Multimedia DirectShow \] \\ \\ \\ \\ Common. Se si copia una cartella di esempio in un'altra directory, assicurarsi di copiare anche la cartella Common.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md)
</dt> </dl>

 

 




