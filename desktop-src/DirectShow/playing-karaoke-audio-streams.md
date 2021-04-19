---
description: Riproduzione di flussi audio karaoke
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Riproduzione di flussi audio karaoke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304089"
---
# <a name="playing-karaoke-audio-streams"></a>Riproduzione di flussi audio karaoke

Il navigatore DVD può riprodurre DVD-Video dischi con flussi audio karaoke, ma la riproduzione karaoke richiede anche un decodificatore che supporta la combinazione di karaoke multicanale. In particolare, il decodificatore deve supportare il [**set di proprietà DVD karaoke**](dvd-karaoke-property-set.md) (AM \_ Property \_ DVDKARAOKE).

I dischi Karaoke sono un tipo di DVD-Video disco e hanno la stessa struttura di navigazione. I brani vengono in genere formattati come titoli e i titoli possono essere raggruppati in set di titoli in base all'esecutore, allo stile musicale o ad altri criteri. La differenza principale tra il karaoke e altri tipi di DVD-Videos è il flusso audio. I dischi Karaoke contengono tutti audio multicanale, in genere Dolby AC-3. I canali 0 e 1 contengono sempre la musica strumentale in background, mentre i canali da 2 a 5 possono contenere qualsiasi combinazione di voce di guida, melodie e effetti audio. Un'applicazione Karaoke può controllare l'altoparlante del volume e della destinazione per ogni canale ausiliario.

Quando il navigatore DVD rileva il contenuto del karaoke su un disco e passa alla modalità karaoke, informa il decodificatore, che dovrebbe quindi disattivare i tre canali più alti (i canali ausiliari) finché nessuno o tutti questi non vengono attivati in modo esplicito da un'applicazione. Le attività di base di un'applicazione karaoke sono:

1.  Determinare il numero di canali ausiliari e il relativo contenuto usando i metodi [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .
2.  Fornire un'interfaccia utente che Visualizza il contenuto del canale e consente agli utenti di attivare o disattivare qualsiasi canale ausiliario in qualsiasi momento usando [**IDVDControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Questi passaggi sono illustrati nell'applicazione di esempio DVD in DVDCore. cpp nel metodo **GetAudioAttributes** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



