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
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="49980-103">Flussi audio e immagine subimmagini</span><span class="sxs-lookup"><span data-stu-id="49980-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="49980-104">Un disco DVD-Video può avere fino a otto flussi audio, numerati da zero a sette, ognuno con un massimo di sei canali discreti.</span><span class="sxs-lookup"><span data-stu-id="49980-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="49980-105">Si noti che i flussi audio e immagine non sono numerati da zero, mentre i titoli, gli angoli e i livelli parentali sono numerati da uno. È possibile selezionare solo uno di questi flussi in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="49980-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="49980-106">Per le immagini secondarie sono disponibili fino a 32 flussi, sebbene sia possibile attivare un solo flusso in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="49980-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="49980-107">I dischi vengono in genere creati con flussi audio e immagine predefiniti, ma un'applicazione può consentire agli utenti di visualizzare un elenco di tutti i flussi disponibili e di selezionare quello nella lingua preferita.</span><span class="sxs-lookup"><span data-stu-id="49980-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="49980-108">I passaggi di base di questo processo sono gli stessi per i flussi audio e di immagine.</span><span class="sxs-lookup"><span data-stu-id="49980-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="49980-109">Determinare il numero di flussi disponibili per un titolo.</span><span class="sxs-lookup"><span data-stu-id="49980-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="49980-110">Scorrere i flussi e recuperare gli attributi del flusso per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="49980-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="49980-111">Recuperare il codice della lingua dall'identificatore delle impostazioni locali (LCID) restituito e creare una stringa leggibile.</span><span class="sxs-lookup"><span data-stu-id="49980-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="49980-112">Popolare una casella di riepilogo o un altro controllo dell'interfaccia utente per consentire all'utente di selezionare un flusso preferito.</span><span class="sxs-lookup"><span data-stu-id="49980-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="49980-113">Nell'applicazione di esempio DVD il metodo CAudioLangDlg:: MakeAudioStreamList in Dialogs. cpp illustra i passaggi di base.</span><span class="sxs-lookup"><span data-stu-id="49980-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49980-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49980-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49980-115">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="49980-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



