---
description: Esempio di playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Esempio di playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309036"
---
# <a name="playlist-sample"></a>Esempio di playlist

Mostra come usare Microsoft Media Foundation per riprodurre una sequenza di file audio in una playlist. Nell'esempio viene utilizzata l' [origine sequencer](sequencer-source.md) per creare e gestire la playlist.

> [!Note]  
> Questo esempio non è più incluso nell'SDK.

 

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Utilizzo

Nell'esempio playlist viene compilata un'applicazione Windows.

-   Per creare una nuova playlist, scegliere **Aggiungi a playlist** dal menu **file** . Nella finestra di dialogo **Apri file** selezionare uno o più file audio. I file vengono aggiunti alla playlist.
-   Per riprodurre la sequenza, fare clic su **Riproduci**.
-   Per sospendere il segmento corrente, fare clic su **Sospendi**.
-   Per arrestare il segmento corrente, fare clic su **Arresta**.
-   Per passare a un file, fare doppio clic sull'elemento nella playlist.
-   Per eliminare un file dalla playlist, selezionare l'elemento nella playlist. Quindi selezionare **Rimuovi dalla playlist** dal menu **file** .

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location                                                     | Percorso/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *Radice SDK* \\ \\ \\ Playlist mediafoundation Multimedia degli esempi \\ |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 
