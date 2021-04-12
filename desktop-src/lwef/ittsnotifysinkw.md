---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398648"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="3a8f1-103">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="3a8f1-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="3a8f1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3a8f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3a8f1-105">Il motore deve chiamare tramite [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)e [**Visual**](https://www.bing.com/search?q=**Visual**).</span><span class="sxs-lookup"><span data-stu-id="3a8f1-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="3a8f1-106">Il callback **visivo** deve fornire fonemi IPA.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="3a8f1-107">(Alfabeto \[ fonetico internazionale) IPA \] è una notazione universale per la descrizione del contenuto fonetico della comunicazione parlata.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="3a8f1-108">Tutti i fonemi pronunciabili presentano rappresentazioni in IPA.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="3a8f1-109">I dettagli del pacchetto IPA si trovano nella parte relativa alla specifica di Microsoft Speech API \[ del download per Speech SDK 4,0 \] all'indirizzo [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3a8f1-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="3a8f1-110">Sebbene la notifica [**visiva**](https://www.bing.com/search?q=**Visual**) sia abbastanza ricca, Microsoft Agent utilizza solo il valore **cIPAPhoneme** per animare la bocca quando il carattere parla.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="3a8f1-111">Qualsiasi motore compatibile con Microsoft Agent deve fornire un flusso strettamente sincronizzato di notifiche **visive** che riflettono il contenuto fonetico della parola prodotta.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="3a8f1-112">In questo caso, "notifica relativamente tempestiva" non è adeguata, perché i relatori sono piuttosto sensibili alle discrepanze tra la posizione della bocca e il contenuto acustico.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="3a8f1-113">Le notifiche **visive** devono essere restituite tempestivamente.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




