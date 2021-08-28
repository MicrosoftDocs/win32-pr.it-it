---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player store online, track.csv
- online store, track.csv
- digitare 1 online stores,track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474917"
---
# <a name="trackcsv"></a>track.csv

Questo file contiene una voce per ogni traccia nel catalogo. Ogni voce è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un intero effettivo.




| Campo | Obbligatoria | Formato | Descrizione | 
|-------|----------|--------|-------------|
| Trackid | Sì | Intero non negativo. Esempio: 32789<br /> | Identificatore univoco fornito dal provider di contenuti. Deve essere minore di 2^32. Suggerimento per le prestazioni: se gli ID assegnati alle tracce dello stesso album sono numerati consecutivamente, la compressione del catalogo sarà più efficiente. Tuttavia, la numerazione consecutiva delle tracce degli album non è necessaria.<br /> | 
| TrackTitle | Sì | Stringa Unicode. Esempio: Raygun Robbers' Blues | Nome della traccia. | 
| Durata | Sì | Intero non negativo. Esempio: 543<br /> | Durata della traccia in secondi. | 
| TrackNumber | Sì | Intero non negativo. Esempio: 7<br /> | Numero di traccia nell'album della traccia. I numeri di traccia iniziano da 1 e aumentano tra i set di dischi. Il numero di traccia deve essere minore di 256. Un numero di traccia maggiore o uguale a 256 causerà un comportamento imprevisto in Windows Media Player. | 
| TrackPrice | Sì | Stringa Unicode. Esempio: $ 0,99. | Tenere traccia del prezzo. Il simbolo di valuta deve essere incluso. La stringa vuota, 0 e , hanno un significato speciale. Una stringa vuota indica che il prezzo è sconosciuto. Uno zero in questo campo indica che la traccia è gratuita e un trattino (-) indica che la traccia non può essere acquistata. | 
| CanStream | Sì | Proprietà di tipo Boolean. Può essere 0 o 1. Esempio: 0<br /> | Indica se la traccia può essere trasmessa. | 
| CanDownload | Sì | Proprietà di tipo Boolean. Può essere 0 o 1. Esempio: 0<br /> | Indica se la traccia può essere scaricata. | 
| HasPreviewClip | Sì | Proprietà di tipo Boolean. Può essere 0 o 1. Esempio: 0<br /> | Indica se la traccia ha un clip di anteprima. | 
| HasVideoClip | Sì | Proprietà di tipo Boolean. Può essere 0 o 1. Esempio: 0<br /> | Indica se la traccia include un clip video. | 
| ParentRating | Sì | Enumerazione. Può essere N, E o C.Esempio: N<br /> | Indica la classificazione di consulenza dei genitori. I valori N, E e C sono Normal, Explicit e Clean. | 
| LinkedAlbumID | Sì | Intero non negativo. Deve essere l'ID di un album. Esempio: 32423 | ID dell'album che contiene questa traccia.<blockquote>[!Note]<br />Ogni traccia deve appartenere a un album. Ciò significa che, per ogni traccia, il campo LinkedAlbumID deve essere uguale a uno degli ID album nel file album.csv.</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | Sì | Elenco di numeri interi. L'elenco contiene gli ID degli artista, separati da punti e virgola. Esempio: 41322;12321; 82123; | Elenco di ID corrispondenti agli autori dei contributi. | 
| Composer | No | Stringa Unicode. Esempio: Innova | Autore della traccia. Se il genere della traccia non ha il campo HasComposer impostato, il valore del campo Composer verrà ignorato. In genere viene usato solo per tracce jazz o classiche. | 
| Popolarità | Sì | Intero non negativo o Float.Esempio: 1252.6<br /> | Determina la posizione della traccia nell'elenco quando viene ordinata in base alla popolarità. Un numero inferiore indica una maggiore popolarità. | 
| StarRating | No | Float.Example: 4.21<br /> | La classificazione a stella verrà arrotondata alla stella 1/4 più vicina Windows Media Player prima di essere visualizzata nell'Windows Media Player utente. | 




 

 

 





