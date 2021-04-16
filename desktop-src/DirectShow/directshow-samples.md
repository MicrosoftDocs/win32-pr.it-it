---
description: Esempi di DirectShow
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: Esempi di DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f58c10615aaaa4305a30934e32ef9b11efb18c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522545"
---
# <a name="directshow-samples"></a>Esempi di DirectShow

Gli esempi di DirectShow sono inclusi nel [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx). Si trovano nel percorso \[ SDK radice \] \\ esempi \\ multimediali \\ DirectShow.

La tabella seguente elenca tutti gli esempi di DirectShow disponibili nella Windows SDK. Per istruzioni su come compilare gli esempi, fare riferimento alla documentazione fornita nella Windows SDK.

Se è presente una documentazione aggiuntiva per un esempio, la prima colonna di questa tabella vi collega.



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
<td><a href="directshow-base-classes.md">Classi base di DirectShow</a></td>
<td>Libreria di classi di base</td>
<td>Classi e funzioni di utilità C++ progettate per l'implementazione di filtri DirectShow.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Esempio AmCap</a></td>
<td>Acquisizione</td>
<td>Applicazione di acquisizione video.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Esempio DVApp</a></td>
<td>Acquisizione</td>
<td>Applicazione di acquisizione video digitale (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Esempio PlayCap</a></td>
<td>Acquisizione</td>
<td>Semplice applicazione di acquisizione.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">Esempio di demo DMO</a></td>
<td>DMO</td>
<td>Trasmette i dati audio da un file WAV tramite un effetto DMO.</td>
<td>DirectX SDK</td>
</tr>
<tr class="even">
<td>Esempio di DVD</td>
<td>DVD</td>
<td>Vengono illustrati la riproduzione e la navigazione con DVD di base, oltre a funzionalità avanzate come la gestione dei livelli padre, i segnalibri, il karaoke e la sincronizzazione dei comandi.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Esempio di filtro InfTee</a></td>
<td>Filtri, varie</td>
<td>Implementazione di esempio del filtro del <a href="infinite-pin-tee-filter.md">pin del pin infinito</a> .</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Esempio di filtro metronomo</a></td>
<td>Filtri, varie</td>
<td>Viene illustrato come implementare un clock di riferimento.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Esempio di filtro del parser PSI</a></td>
<td>Filtri, varie</td>
<td>Riceve le tabelle di informazioni specifiche del programma da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Esempio di filtro dump</a></td>
<td>Filtri, renderer</td>
<td>Scrive esempi di supporti ricevuti in un file di testo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Filtro SampVid</td>
<td>Filtri, renderer</td>
<td>Filtro renderer video.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Esempio di filtro di ambito</a></td>
<td>Filtri, renderer</td>
<td>Visualizza i dati audio come moduli Wave.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Esempio di filtro asincrono</a></td>
<td>Filtri, origine</td>
<td>Filtro di lettura file che supporta il download progressivo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Esempio di filtro palla</a></td>
<td>Filtri, origine</td>
<td>Filtro origine video che produce un'immagine di una palla da rimbalzo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Esempio di filtri di origine push</a></td>
<td>Filtri, origine</td>
<td>Filtri di origine che forniscono i dati seguenti come flusso video: una singola bitmap, un set di bitmap, una copia dell'immagine desktop corrente.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Esempio di filtro synth</a></td>
<td>Filtri, origine</td>
<td>Filtro di origine che genera le forme d'onda audio. Questo esempio illustra la creazione di grafici dinamici.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Esempio di filtro EZRGB24</a></td>
<td>Filtri, trasformazione</td>
<td>Filtro di elaborazione immagini.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Esempio di filtro gargarismi</a></td>
<td>Filtri, trasformazione</td>
<td>Filtro effetti audio.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Esempio di filtro WavDest</a></td>
<td>Filtri, trasformazione</td>
<td>Scrive un flusso audio in un file WAV.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Esempio DMOEnum</a></td>
<td>Varie</td>
<td>Viene illustrato come enumerare <a href="directx-media-objects.md">oggetti multimediali DirectX</a> (DMOS).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Esempio di Mapper</a></td>
<td>Varie</td>
<td>Viene illustrato come utilizzare il <a href="filter-mapper.md">mapper del filtro</a> per trovare i filtri nel registro di sistema.</td>

</tr>
<tr class="even">
<td>Esempio SysEnum</td>
<td>Varie</td>
<td>Viene illustrato l'utilizzo di <a href="system-device-enumerator.md">System Device Enumerator</a> per enumerare i dispositivi e i filtri.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Esempio di filmato</a></td>
<td>Riproduzione</td>
<td>Riproduce un file video in modalità schermo intero.</td>

</tr>
<tr class="even">
<td>Esempio DDrawXCL</td>
<td>Riproduzione</td>
<td>Riproduce video in modalità a schermo intero esclusivo di DirectDraw, usando l'interfaccia <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> sul filtro per il <a href="overlay-mixer-filter.md">mixer della sovrimpressione</a> .</td>

</tr>
<tr class="odd">
<td>Esempio DShowPlayer</td>
<td>Riproduzione</td>
<td>Applicazione di riproduzione video.</td>

</tr>
<tr class="even">
<td>Esempio EVRPlayer</td>
<td>Riproduzione</td>
<td>Viene illustrato come usare il filtro EVR DirectShow.
<blockquote>
[!Note]<br />
Richiede Windows Vista o versione successiva.
</blockquote>
<br/> <br/> Questo esempio è disponibile nella Windows SDK per Windows Server 2008 o versione successiva.<br/></td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Esempio Texture3D9</td>
<td>Riproduzione</td>
<td>Disegna il video in una superficie di trama Microsoft DirectX 9,0.</td>
<td>strmbase. lib, DirectX SDK</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Esempio di riquadro di selezione</a></td>
<td>VMR-9</td>
<td>USA VMR-9 per mescolare il video e il testo.</td>

</tr>
<tr class="odd">
<td>Esempio VMR9Allocator</td>
<td>VMR-9</td>
<td>Implementa un allocatore-Presenter personalizzato per VMR-9.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td>Esempio VMR9Compositor</td>
<td>VMR-9</td>
<td>Implementa un mixer personalizzato per VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Esempio VMRPlayer</a></td>
<td>VMR-9</td>
<td>USA VMR-9 per unire uno o due video in esecuzione e un'immagine statica.</td>

</tr>
<tr class="even">
<td>Esempio di filigrana</td>
<td>VMR-9</td>
<td>Combina una bitmap statica su un video durante la riproduzione, usando VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Esempio senza finestra</a></td>
<td>VMR-9</td>
<td>Viene illustrata la modalità senza finestra in VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dipendenze aggiuntive

Alcuni degli esempi sono collegati alla libreria di classi base DirectShow. Per compilare questi esempi, è necessario innanzitutto compilare la libreria di classi di base. Per altre informazioni, vedere [classi base di DirectShow](directshow-base-classes.md). La libreria di classi di base è obbligatoria per tutti i filtri di esempio.

Alcuni esempi richiedono anche DirectX SDK, oltre all'Windows SDK. Per compilare questi esempi, è necessario installare DirectX SDK e impostare la \_ variabile di ambiente% DXSDK dir% uguale al percorso di installazione di DirectX SDK.

Molti esempi di DirectShow usano un set di intestazioni e file di origine comuni che si trovano in directrory \[ SDK root \] \\ Samples \\ Multimedia \\ DirectShow \\ Common. Se si copia una cartella di esempio in un'altra directory, assicurarsi di copiare anche la cartella comune.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md)
</dt> </dl>

 

 




