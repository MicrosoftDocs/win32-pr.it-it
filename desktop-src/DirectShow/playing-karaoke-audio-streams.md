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
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="7eafb-103">Riproduzione di flussi audio karaoke</span><span class="sxs-lookup"><span data-stu-id="7eafb-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="7eafb-104">Il navigatore DVD può riprodurre DVD-Video dischi con flussi audio karaoke, ma la riproduzione karaoke richiede anche un decodificatore che supporta la combinazione di karaoke multicanale.</span><span class="sxs-lookup"><span data-stu-id="7eafb-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="7eafb-105">In particolare, il decodificatore deve supportare il [**set di proprietà DVD karaoke**](dvd-karaoke-property-set.md) (AM \_ Property \_ DVDKARAOKE).</span><span class="sxs-lookup"><span data-stu-id="7eafb-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="7eafb-106">I dischi Karaoke sono un tipo di DVD-Video disco e hanno la stessa struttura di navigazione.</span><span class="sxs-lookup"><span data-stu-id="7eafb-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="7eafb-107">I brani vengono in genere formattati come titoli e i titoli possono essere raggruppati in set di titoli in base all'esecutore, allo stile musicale o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="7eafb-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="7eafb-108">La differenza principale tra il karaoke e altri tipi di DVD-Videos è il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="7eafb-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="7eafb-109">I dischi Karaoke contengono tutti audio multicanale, in genere Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="7eafb-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="7eafb-110">I canali 0 e 1 contengono sempre la musica strumentale in background, mentre i canali da 2 a 5 possono contenere qualsiasi combinazione di voce di guida, melodie e effetti audio.</span><span class="sxs-lookup"><span data-stu-id="7eafb-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="7eafb-111">Un'applicazione Karaoke può controllare l'altoparlante del volume e della destinazione per ogni canale ausiliario.</span><span class="sxs-lookup"><span data-stu-id="7eafb-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="7eafb-112">Quando il navigatore DVD rileva il contenuto del karaoke su un disco e passa alla modalità karaoke, informa il decodificatore, che dovrebbe quindi disattivare i tre canali più alti (i canali ausiliari) finché nessuno o tutti questi non vengono attivati in modo esplicito da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7eafb-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="7eafb-113">Le attività di base di un'applicazione karaoke sono:</span><span class="sxs-lookup"><span data-stu-id="7eafb-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="7eafb-114">Determinare il numero di canali ausiliari e il relativo contenuto usando i metodi [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .</span><span class="sxs-lookup"><span data-stu-id="7eafb-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="7eafb-115">Fornire un'interfaccia utente che Visualizza il contenuto del canale e consente agli utenti di attivare o disattivare qualsiasi canale ausiliario in qualsiasi momento usando [**IDVDControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span><span class="sxs-lookup"><span data-stu-id="7eafb-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="7eafb-116">Questi passaggi sono illustrati nell'applicazione di esempio DVD in DVDCore. cpp nel metodo **GetAudioAttributes** .</span><span class="sxs-lookup"><span data-stu-id="7eafb-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eafb-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7eafb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eafb-118">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="7eafb-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



