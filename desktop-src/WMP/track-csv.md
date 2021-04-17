---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online Stores, track.csv
- archivi online, track.csv
- digitare 1 Store online, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330660"
---
# <a name="trackcsv"></a>track.csv

Questo file contiene una voce per ogni traccia nel catalogo. Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Necessario</th>
<th>Formato</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TrackID</td>
<td>Sì</td>
<td>Integer non negativo. Esempio: 32789<br/></td>
<td>Identificatore univoco fornito dal provider di contenuti. Deve essere minore di 2 ^ 32. suggerimento per le prestazioni: se gli ID assegnati alle tracce dello stesso album sono numerati consecutivamente, la compressione del catalogo sarà più efficiente. Tuttavia, la numerazione consecutiva delle tracce di album non è obbligatoria.<br/></td>
</tr>
<tr class="even">
<td>TrackTitle</td>
<td>Sì</td>
<td>Stringa Unicode. Esempio: Raygun Robbers ' Blues</td>
<td>Nome della traccia.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Sì</td>
<td>Integer non negativo. Esempio: 543<br/></td>
<td>Durata della traccia in secondi.</td>
</tr>
<tr class="even">
<td>Numero</td>
<td>Sì</td>
<td>Integer non negativo. Esempio: 7<br/></td>
<td>Numero di traccia nell'album della traccia. I numeri di traccia iniziano da 1 e aumentano tra i set di dischi. Il numero di traccia deve essere minore di 256. Un numero di traccia maggiore o uguale a 256 provocherà un comportamento imprevisto in Windows Media Player.</td>
</tr>
<tr class="odd">
<td>TrackPrice</td>
<td>Sì</td>
<td>Stringa Unicode. Esempio: $0,99.</td>
<td>Tenere traccia del prezzo. È necessario includere il simbolo di valuta. La stringa vuota, 0 e-hanno un significato speciale. Una stringa vuota indica che il prezzo è sconosciuto. Uno zero in questo campo indica che la traccia è gratuita e un trattino (-) indica che non è possibile acquistare la traccia.</td>
</tr>
<tr class="even">
<td>CanStream</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1. esempio: 0<br/></td>
<td>Indica se è possibile trasmettere la traccia.</td>
</tr>
<tr class="odd">
<td>CanDownload</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1. esempio: 0<br/></td>
<td>Indica se è possibile scaricare la traccia.</td>
</tr>
<tr class="even">
<td>HasPreviewClip</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1. esempio: 0<br/></td>
<td>Indica se la traccia include una clip di anteprima.</td>
</tr>
<tr class="odd">
<td>HasVideoClip</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1. esempio: 0<br/></td>
<td>Indica se la traccia contiene un clip video.</td>
</tr>
<tr class="even">
<td>ParentalRating</td>
<td>Sì</td>
<td>Enumerazione. Può essere N, E o C. esempio: N<br/></td>
<td>Indica la classificazione consultiva padre. I valori N, e e C sono i valori normali, espliciti e puliti.</td>
</tr>
<tr class="odd">
<td>LinkedAlbumID</td>
<td>Sì</td>
<td>Integer non negativo. Deve corrispondere all'ID di un album. Esempio: 32423</td>
<td>ID dell'album che contiene la traccia.
<blockquote>
[!Note]<br />
Ogni traccia deve appartenere a un album. Ovvero, per ogni traccia, il campo LinkedAlbumID deve essere uguale a uno degli ID album nel file album.csv.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Sì</td>
<td>Elenco di numeri interi. L'elenco contiene gli ID degli artisti, separati da punti e virgola. Esempio: 41322; 12321; 82123;</td>
<td>Elenco di ID corrispondenti agli artisti che contribuiscono.</td>
</tr>
<tr class="odd">
<td>Composer</td>
<td>No</td>
<td>Stringa Unicode. Esempio: Beethoven</td>
<td>Compositore della traccia. Se per il genere della traccia non è impostato il campo HasComposer, il valore del campo Composer verrà ignorato. Usato in genere solo per le tracce jazz o classiche.</td>
</tr>
<tr class="even">
<td>Popolarità</td>
<td>Sì</td>
<td>Intero non negativo o float. esempio: 1252,6<br/></td>
<td>Determina la posizione della traccia nell'elenco quando è ordinata in base alla popolarità. Un numero inferiore indica una maggiore popolarità.</td>
</tr>
<tr class="odd">
<td>StarRating</td>
<td>No</td>
<td>Float. esempio: 4,21<br/></td>
<td>La classificazione a stelle verrà arrotondata al più vicino a 1/4 stelle da Windows Media Player prima di essere visualizzata nell'interfaccia utente di Windows Media Player.</td>
</tr>
</tbody>
</table>



 

 

 





