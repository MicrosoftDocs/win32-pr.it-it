---
description: Un numero di factoids descrive l'input comune a tutti i riconoscitori del linguaggio e non deve avere formati diversi per le diverse lingue. La tabella seguente elenca factoids comuni in tutti i linguaggi.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids comuni tra lingue diverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307492"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="dc771-104">Factoids comuni tra lingue diverse</span><span class="sxs-lookup"><span data-stu-id="dc771-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="dc771-105">Un numero di factoids descrive l'input comune a tutti i riconoscitori del linguaggio e non deve avere formati diversi per le diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="dc771-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="dc771-106">La tabella seguente elenca factoids comuni in tutti i linguaggi.</span><span class="sxs-lookup"><span data-stu-id="dc771-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc771-107">Factoid</span><span class="sxs-lookup"><span data-stu-id="dc771-107">Factoid</span></span></th>
<th><span data-ttu-id="dc771-108">Definizione</span><span class="sxs-lookup"><span data-stu-id="dc771-108">Definition</span></span></th>
<th><span data-ttu-id="dc771-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc771-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc771-110"><strong>Cifre</strong></span><span class="sxs-lookup"><span data-stu-id="dc771-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="dc771-111">Imposta la distorsione per una singola cifra.</span><span class="sxs-lookup"><span data-stu-id="dc771-111">Sets bias for a single digit.</span></span> <span data-ttu-id="dc771-112">Il riconoscimento è distorto per restituire solo le cifre singole quando questo controllo è impostato.</span><span class="sxs-lookup"><span data-stu-id="dc771-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="dc771-113">0-9</span><span class="sxs-lookup"><span data-stu-id="dc771-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc771-114"><strong>Posta elettronica</strong></span><span class="sxs-lookup"><span data-stu-id="dc771-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="dc771-115">Imposta la distorsione per un indirizzo di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="dc771-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc771-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="dc771-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="dc771-117">Imposta la distorsione per diversi formati di URL.</span><span class="sxs-lookup"><span data-stu-id="dc771-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc771-118">Le impostazioni predefinite per il riconoscimento includono il controllo <strong>Web</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc771-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="dc771-119">Per questo motivo, è possibile che non si noti una grande differenza tra il controllo dell'oggetto <strong>Web</strong> e l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dc771-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="dc771-120">Tuttavia, il controllo <strong>Web</strong> consente di eliminare gli spazi tra le parole in un URL.</span><span class="sxs-lookup"><span data-stu-id="dc771-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="dc771-121">http: \\ Microsoft.NET</span><span class="sxs-lookup"><span data-stu-id="dc771-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="dc771-122">https: \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="dc771-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="dc771-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="dc771-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="dc771-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="dc771-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="dc771-125">http: \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="dc771-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="dc771-126">http: \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="dc771-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="dc771-127">http: \\ www. Microsoft. com\myfile.asp</span><span class="sxs-lookup"><span data-stu-id="dc771-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="dc771-128">http: \\ www.Microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="dc771-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="dc771-129">http: \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="dc771-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="dc771-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="dc771-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc771-131"><strong>Default</strong></span><span class="sxs-lookup"><span data-stu-id="dc771-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="dc771-132">Restituisce le impostazioni predefinite del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="dc771-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="dc771-133">L'impostazione predefinita per factoids per le lingue occidentali include il dizionario di sistema, il dizionario utenti, le varie punteggiatura e il factoids <strong>Web</strong> e il <strong>numero</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc771-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="dc771-134">L'impostazione predefinita per factoids per le lingue asiatiche orientali include tutti i caratteri supportati dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="dc771-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc771-135"><strong>Nessuno</strong></span><span class="sxs-lookup"><span data-stu-id="dc771-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="dc771-136">Disabilita tutti factoids, dizionari e il modello di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="dc771-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="dc771-137">Questo controllo del controllo deve essere usato solo quando non si vuole che il riconoscimento usi alcuna regola di grammatica o dizionari, incluso il dizionario di sistema.</span><span class="sxs-lookup"><span data-stu-id="dc771-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="dc771-138">Questo controllo è utile per l'input di stringhe casuali, ad esempio codici prodotto.</span><span class="sxs-lookup"><span data-stu-id="dc771-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="dc771-139">Non usare il flag di coercizione con questo controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="dc771-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




