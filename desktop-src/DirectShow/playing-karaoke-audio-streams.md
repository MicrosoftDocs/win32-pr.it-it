---
description: Riproduzione di contenuti audio per il Flussi
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Riproduzione di contenuti audio per il Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10912761034feb9ed82c85625324cd3091514b2c492c66b4e49af711d7d2152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213301"
---
# <a name="playing-karaoke-audio-streams"></a>Riproduzione di contenuti audio per il Flussi

Lo strumento di navigazione DVD può riprodurre DVD-Video dischi con flussi audio di tipo stereo, ma per la riproduzione del tutto stereo è necessario anche un decodificatore che supporti la combinazione multicanale per il mixaggio per il tutto multicanale. In particolare, il decodificatore deve supportare il set di proprietà [**DVD Karaoke**](dvd-karaoke-property-set.md) (AM PROPERTY \_ \_ DVDKARAOKE).

I dischi Disassato sono un tipo DVD-Video disco e hanno la stessa struttura di navigazione. I brani sono in genere formattati come titoli e i titoli possono essere raggruppati in set di titoli in base all'esecutore, allo stile musicale o ad altri criteri. La differenza principale tra il karaoke e altri tipi di DVD-Videos è il flusso audio. I dischi Disaborso contengono tutti audio multicanale, in genere Dolby AC-3. I canali 0 e 1 contengono sempre la musica strumentale di sottofondo, mentre i canali da 2 a 5 possono contenere ogni combinazione di guide vocali, linee guida ed effetti sonori. Un'applicazione per il mirroring può controllare il volume e l'altoparlante di destinazione per ogni canale ausiliario.

Quando lo strumento di spostamento DVD rileva il contenuto di un disco e passa alla modalità di visualizzazione del contenuto, informa il decodificatore, che dovrebbe disattivare i tre canali superiori (i canali ausiliari) fino a quando uno o tutti i canali non vengono attivati in modo esplicito da un'applicazione. Le attività di base di un'applicazione di questo tipo sono:

1.  Determinare il numero di canali ausiliari e il relativo contenuto [**usando i metodi IDvdInfo2.**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)
2.  Fornire un'interfaccia utente che visualizza il contenuto del canale e consente agli utenti di attivare o disattivare qualsiasi canale ausiliario in qualsiasi momento, usando [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Questi passaggi sono illustrati nell'applicazione DVD Sample in DVDCore.cpp nel **metodo GetAudioAttributes.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



