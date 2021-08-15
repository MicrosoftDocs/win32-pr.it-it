---
description: Esempio di playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Esempio di playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cad2ef96c76512947a5b74e7eac54e3ad5787218e625f30fea5b8e5164177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239128"
---
# <a name="playlist-sample"></a>Esempio di playlist

Illustra come usare Microsoft Media Foundation per riprodurre una sequenza di file audio in una playlist. L'esempio usa [l'origine Sequencer](sequencer-source.md) per creare e gestire la playlist.

> [!Note]  
> Questo esempio non è più incluso nell'SDK.

 

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Media Foundation seguenti:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Utilizzo

L'esempio Playlist compila un'Windows applicazione.

-   Per creare una nuova playlist, **scegliere Aggiungi a playlist** dal menu **File.** Nella finestra **di dialogo Apri** file selezionare uno o più file audio. I file vengono aggiunti alla playlist.
-   Per riprodurre la sequenza, fare clic su **Riproduci.**
-   Per sospendere il segmento corrente, fare clic su **Sospendi.**
-   Per arrestare il segmento corrente, fare clic su **Arresta**.
-   Per passare a un file, fare doppio clic sull'elemento nella playlist.
-   Per eliminare un file dalla playlist, selezionare l'elemento nella playlist. Selezionare quindi **Rimuovi dalla playlist** dal menu **File.**

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Percorso                                                     | Percorso/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *RADICE DELL'SDK* \\ Playlist \\ \\ mediafoundation \\ multimediale di esempio |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 
