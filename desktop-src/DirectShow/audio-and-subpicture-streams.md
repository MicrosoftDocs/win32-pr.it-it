---
description: Audio and Subpicture Flussi
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Audio and Subpicture Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f553b5e569274cf7abafd34e897ba53f82e0292899661fb47ace9ada92dd84f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001363"
---
# <a name="audio-and-subpicture-streams"></a>Audio and Subpicture Flussi

Un DVD-Video può avere fino a otto flussi audio, numerati da zero a sette, ognuno con un massimo di sei canali discreti. Si noti che i flussi audio e di immagini secondarie sono numerati da zero, mentre i titoli, le angolazioni e i livelli dei genitori sono numerati da uno. È possibile selezionare solo uno di questi flussi in un determinato momento. Per le immagini secondarie sono disponibili fino a 32 flussi, anche se è possibile attivare un solo flusso in un determinato momento. I dischi vengono in genere creati con flussi audio e di immagini secondarie predefiniti, ma un'applicazione può consentire agli utenti di visualizzare un elenco di tutti i flussi disponibili e selezionare quello nella lingua preferita. I passaggi di base di questo processo sono gli stessi sia per i flussi audio che per i flussi di immagini secondarie.

1.  Determinare il numero di flussi disponibili per un titolo.
2.  Scorrere i flussi e recuperare gli attributi del flusso per ognuno.
3.  Recuperare il codice lingua dall'identificatore delle impostazioni locali (LCID) restituito e creare una stringa leggibile.
4.  Popolare una casella di riepilogo o un altro controllo dell'interfaccia utente per consentire all'utente di selezionare un flusso preferito.

Nell'applicazione di esempio DVD, il metodo CAudioLangDlg::MakeAudioStreamList in Dialogs.cpp illustra i passaggi di base.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



