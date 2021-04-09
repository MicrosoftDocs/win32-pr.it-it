---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955772"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="85af1-103">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="85af1-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="85af1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85af1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="85af1-105">Il motore deve chiamare tramite **segnalibro**.</span><span class="sxs-lookup"><span data-stu-id="85af1-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="85af1-106">Durante la pre-elaborazione dell'output vocale, il codice dell'agente Microsoft inserisce segnalibri tra "parole" e usa l'arrivo di tali segnalibri per guidare la velocità del testo nel fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="85af1-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="85af1-107">Sebbene SAPI non richieda più dell'arrivo di questi segnalibri in un determinato momento prima della fine dell'espressione, i segnalibri devono essere restituiti in modo relativamente tempestivo per supportare Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="85af1-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="85af1-108">Si noti che non esiste un concetto rigoroso di "parola" in alcune lingue, ad esempio il giapponese.</span><span class="sxs-lookup"><span data-stu-id="85af1-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="85af1-109">Il metodo [**Speak**](speak-method.md) di Microsoft Agent definisce una "parola" come una stringa connessa di simboli con un significato e una pronuncia in isolamento.</span><span class="sxs-lookup"><span data-stu-id="85af1-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="85af1-110">Microsoft Agent usa un codice di analisi piuttosto semplice per determinare la "parola": Cerca i simboli separati da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="85af1-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="85af1-111">Ci sono quindi tre "parole" nella stringa inglese "The 101 Dalmati": "The", "101" e "Dalmati".</span><span class="sxs-lookup"><span data-stu-id="85af1-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="85af1-112">Il testo incluso nel tag della mappa di Microsoft Agent viene considerato come una singola parola a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="85af1-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




