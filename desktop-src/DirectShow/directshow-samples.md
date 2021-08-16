---
description: DirectShow Campioni
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Campioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb99271821fcef80b66b379b29bd42de0505011fd47c8dfee208e6f00b007208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821166"
---
# <a name="directshow-samples"></a>DirectShow Campioni

Gli DirectShow seguenti sono inclusi in [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx). Si trovano nel percorso \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

La tabella seguente elenca tutti gli esempi DirectShow disponibili in Windows SDK. Per istruzioni su come compilare gli esempi, vedere la documentazione fornita in Windows SDK.

Se è disponibile documentazione aggiuntiva per un esempio, la prima colonna di questa tabella è collegata ad essa.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Esempio</th>
<th>Area</th>
<th>Descrizione</th>
<th>Dipendenze aggiuntive</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">DirectShow Classi di base</a></td>
<td>Libreria di classi di base</td>
<td>Classi C++ e funzioni di utilità progettate per l'implementazione DirectShow filtri.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Esempio AmCap</a></td>
<td>Acquisizione</td>
<td>Applicazione di acquisizione video.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Esempio di DVApp</a></td>
<td>Acquisizione</td>
<td>Applicazione di acquisizione di video digitali (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Esempio PlayCap</a></td>
<td>Acquisizione</td>
<td>Applicazione di acquisizione semplice.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO Esempio dimostrativo</a></td>
<td>DMO</td>
<td>Flussi dati audio da un file WAV tramite un effetto audio DMO.</td>
<td>DirectX SDK</td>
</tr>
<tr class="even">
<td>Esempio di DVD</td>
<td>DVD</td>
<td>Illustra la riproduzione e la navigazione dei DVD di base, oltre a funzionalità avanzate come la gestione a livello di genitori, i segnalibri, la sincronizzazione dei comandi e dei dvd.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Esempio di filtro InfTee</a></td>
<td>Filtri, vari</td>
<td>Implementazione di esempio del <a href="infinite-pin-tee-filter.md">filtro Infinite Pin Tee.</a></td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Esempio di filtro metronome</a></td>
<td>Filtri, vari</td>
<td>Illustra come implementare un clock di riferimento.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Esempio di filtro del parser PSI</a></td>
<td>Filtri, vari</td>
<td>Riceve le tabelle PSI (Program Specific Information) da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Esempio di filtro dump</a></td>
<td>Filtri, renderer</td>
<td>Scrive gli esempi multimediali ricevuti in un file di testo.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>Filtro SampVid</td>
<td>Filtri, renderer</td>
<td>Filtro del renderer video.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Esempio di filtro ambito</a></td>
<td>Filtri, renderer</td>
<td>Visualizza i dati audio come forme d'onda.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Esempio di filtro asincrono</a></td>
<td>Filtri, origine</td>
<td>Filtro lettore di file che supporta il download progressivo.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Esempio di filtro palla</a></td>
<td>Filtri, origine</td>
<td>Filtro di origine video che produce un'immagine di una palla che si rigonfia.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Esempio di filtri origine push</a></td>
<td>Filtri, origine</td>
<td>Filtri di origine che forniscono i dati seguenti come flusso video: una singola bitmap, un set di bitmap, una copia dell'immagine desktop corrente.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Esempio di filtro synth</a></td>
<td>Filtri, origine</td>
<td>Filtro di origine che genera forme d'onda audio. Questo esempio illustra la creazione dinamica di grafi.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Esempio di filtro EZRGB24</a></td>
<td>Filtri, trasformazione</td>
<td>Filtro di elaborazione delle immagini.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Esempio di filtro Gargle</a></td>
<td>Filtri, trasformazione</td>
<td>Filtro dell'effetto audio.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Esempio di filtro WavDest</a></td>
<td>Filtri, trasformazione</td>
<td>Scrive un flusso audio in un file WAV.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Esempio DMOEnum</a></td>
<td>Varie</td>
<td>Illustra come enumerare <a href="directx-media-objects.md">oggetti multimediali DirectX</a> (DMO).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Esempio di mapper</a></td>
<td>Varie</td>
<td>Illustra come usare Filter <a href="filter-mapper.md">Mapper per</a> trovare i filtri nel Registro di sistema.</td>

</tr>
<tr class="even">
<td>Esempio SysEnum</td>
<td>Varie</td>
<td>Illustra l'uso di <a href="system-device-enumerator.md">System Device Enumerator</a> per enumerare dispositivi e filtri.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Esempio di CutScene</a></td>
<td>Riproduzione</td>
<td>Riproduce un file video in modalità schermo intero.</td>

</tr>
<tr class="even">
<td>Esempio di DDrawXCL</td>
<td>Riproduzione</td>
<td>Riproduce video in modalità schermo intero esclusiva DirectDraw, usando <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>l'interfaccia IDDrawExclModeVideo</strong></a> nel filtro di Mixer sovrimpressione. <a href="overlay-mixer-filter.md"></a></td>

</tr>
<tr class="odd">
<td>Esempio di DShowPlayer</td>
<td>Riproduzione</td>
<td>Applicazione di riproduzione video.</td>

</tr>
<tr class="even">
<td>Esempio di EVRPlayer</td>
<td>Riproduzione</td>
<td>Illustra come usare il filtro DirectShow EVR.
<blockquote>
[!Note]<br />
Richiede Windows Vista o versione successiva.
</blockquote>
<br/> <br/> Questo esempio è disponibile in Windows SDK per Windows Server 2008 o versione successiva.<br/></td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>Esempio texture3D9</td>
<td>Riproduzione</td>
<td>Disegna video su una superficie di trama di Microsoft DirectX 9.0.</td>
<td>strmbase.lib, DirectX SDK</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Esempio di Ticker</a></td>
<td>VMR-9</td>
<td>Usa VMR-9 per unire video e testo.</td>

</tr>
<tr class="odd">
<td>Esempio di VMR9Allocator</td>
<td>VMR-9</td>
<td>Implementa un allocatore-presenter personalizzato per vmr-9.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td>Esempio di VMR9Compositor</td>
<td>VMR-9</td>
<td>Implementa un mixer personalizzato per VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Esempio di VMRPlayer</a></td>
<td>VMR-9</td>
<td>Usa VMR-9 per unire uno o due video in esecuzione e un'immagine statica.</td>

</tr>
<tr class="even">
<td>Esempio di filigrana</td>
<td>VMR-9</td>
<td>Unisce una bitmap statica a un video durante la riproduzione, usando vmr-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Esempio senza finestra</a></td>
<td>VMR-9</td>
<td>Illustra la modalità senza finestra in VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dipendenze aggiuntive

Alcuni esempi si collegano alla libreria DirectShow di classi di base. Per compilare questi esempi, è prima necessario compilare la libreria di classi di base. Per altre informazioni, vedere Classi [DirectShow base](directshow-base-classes.md). La libreria di classi di base è necessaria per tutti i filtri di esempio.

Alcuni esempi richiedono anche DirectX SDK, oltre a Windows SDK. Per compilare questi esempi, è necessario installare DirectX SDK e impostare la variabile di ambiente %DXSDK DIR% uguale al percorso di installazione \_ di DirectX SDK.

Molti esempi di DirectShow usano un set di intestazioni e file di origine comuni che si trovano in Directrory \[ SDK Root Samples Multimedia DirectShow \] \\ \\ \\ \\ Common. Se si copia una cartella di esempio in un'altra directory, assicurarsi di copiare anche la cartella Common.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md)
</dt> </dl>

 

 




