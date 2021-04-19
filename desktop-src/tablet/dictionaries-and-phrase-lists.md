---
description: Il lessico o l'elenco di parole possibili usate dal modello di linguaggio di un particolare riconoscitore sono contenuti in uno o più dizionari.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dizionari ed elenchi di frasi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316854"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="8890f-103">Dizionari ed elenchi di frasi</span><span class="sxs-lookup"><span data-stu-id="8890f-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="8890f-104">Il lessico o l'elenco di parole possibili usate dal modello di linguaggio di un particolare riconoscitore sono contenuti in uno o più dizionari.</span><span class="sxs-lookup"><span data-stu-id="8890f-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="8890f-105">Il riconoscitore Cerca tutti i dizionari disponibili nel sistema durante la compilazione delle corrispondenze di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8890f-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="8890f-106">Per modificare alcuni di questi dizionari, è possibile usare le API Microsoft Speech (SAPI).</span><span class="sxs-lookup"><span data-stu-id="8890f-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="8890f-107">Un elenco di frasi fornisce un altro mezzo per modificare il vocabolario del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="8890f-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="8890f-108">L'aggiunta di parole a un elenco di frasi estende il vocabolario; l'aggiunta di parole e la limitazione del riconoscimento per l'utilizzo solo dell'elenco di frasi (in contrapposizione all'elenco di frasi e ai dizionari) limitano il vocabolario.</span><span class="sxs-lookup"><span data-stu-id="8890f-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="8890f-109">Le versioni precedenti delle API della tecnologia Tablet PC si basavano sul concetto di elenchi di parole.</span><span class="sxs-lookup"><span data-stu-id="8890f-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="8890f-110">Gli elenchi di parole sono quasi identici agli elenchi di frasi e vengono usati per lo stesso scopo quando si lavora direttamente con un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) in un'applicazione abilitata per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="8890f-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="8890f-111">Per altre informazioni su dove e quando usare gli elenchi di parole, vedere [impostazione del contesto per i controlli Ink-Enabled](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8890f-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="8890f-112">Quando le dimensioni dell'elenco con cui si desidera estendere il lessico superano 100.000 parole, è consigliabile utilizzare un dizionario anziché un elenco di parole o una frase.</span><span class="sxs-lookup"><span data-stu-id="8890f-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



