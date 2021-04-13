---
description: Flussi audio e immagine subimmagini
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Flussi audio e immagine subimmagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482533"
---
# <a name="audio-and-subpicture-streams"></a>Flussi audio e immagine subimmagini

Un disco DVD-Video può avere fino a otto flussi audio, numerati da zero a sette, ognuno con un massimo di sei canali discreti. Si noti che i flussi audio e immagine non sono numerati da zero, mentre i titoli, gli angoli e i livelli parentali sono numerati da uno. È possibile selezionare solo uno di questi flussi in un determinato momento. Per le immagini secondarie sono disponibili fino a 32 flussi, sebbene sia possibile attivare un solo flusso in un determinato momento. I dischi vengono in genere creati con flussi audio e immagine predefiniti, ma un'applicazione può consentire agli utenti di visualizzare un elenco di tutti i flussi disponibili e di selezionare quello nella lingua preferita. I passaggi di base di questo processo sono gli stessi per i flussi audio e di immagine.

1.  Determinare il numero di flussi disponibili per un titolo.
2.  Scorrere i flussi e recuperare gli attributi del flusso per ciascuno di essi.
3.  Recuperare il codice della lingua dall'identificatore delle impostazioni locali (LCID) restituito e creare una stringa leggibile.
4.  Popolare una casella di riepilogo o un altro controllo dell'interfaccia utente per consentire all'utente di selezionare un flusso preferito.

Nell'applicazione di esempio DVD il metodo CAudioLangDlg:: MakeAudioStreamList in Dialogs. cpp illustra i passaggi di base.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



