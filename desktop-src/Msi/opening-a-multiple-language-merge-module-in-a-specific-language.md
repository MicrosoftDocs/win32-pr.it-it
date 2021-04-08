---
description: Quando si esegue il merge di un modulo in un database di installazione, sono disponibili due linguaggi importanti.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Apertura di un modulo merge Multiple-Language in una lingua specifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049624"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="77602-103">Apertura di un modulo merge Multiple-Language in una lingua specifica</span><span class="sxs-lookup"><span data-stu-id="77602-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="77602-104">Quando si esegue il merge di un modulo in un database di installazione, sono disponibili due linguaggi importanti.</span><span class="sxs-lookup"><span data-stu-id="77602-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="77602-105">Il primo è la lingua del pacchetto di installazione di destinazione specificato da [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="77602-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="77602-106">Il secondo è il linguaggio del modulo merge visualizzato nella colonna language della [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="77602-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="77602-107">La lingua del pacchetto di installazione può essere passata al modulo dallo strumento di merge quando il pacchetto viene aperto per un'operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="77602-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="77602-108">Tuttavia, a volte potrebbe essere necessario ignorare la lingua della destinazione e richiedere che il modulo venga aperto in un'altra lingua, ad esempio un pacchetto inglese che installa sia le risorse inglesi che quelle tedesche dal modulo.</span><span class="sxs-lookup"><span data-stu-id="77602-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="77602-109">Quando si apre un modulo con una richiesta di lingua, lo strumento di merge controlla la lingua richiesta rispetto alle lingue specificate nella colonna lingua della [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="77602-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="77602-110">Il processo seguente viene usato per determinare la lingua da usare.</span><span class="sxs-lookup"><span data-stu-id="77602-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="77602-111">**Per determinare la lingua da usare**</span><span class="sxs-lookup"><span data-stu-id="77602-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="77602-112">Se la lingua nella [tabella ModuleSignature](modulesignature-table.md) è uguale o più generale rispetto alla lingua richiesta, viene aperto il modulo.</span><span class="sxs-lookup"><span data-stu-id="77602-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="77602-113">Se il modulo supporta la lingua esatta richiesta, viene usata tale lingua.</span><span class="sxs-lookup"><span data-stu-id="77602-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="77602-114">Se il modulo supporta il gruppo di lingue della lingua richiesta dal gruppo di lingue, ad esempio, controllare 9 se 1033 è stato richiesto ma non è stato trovato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="77602-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="77602-115">Controllare se è presente una trasformazione del linguaggio che modifica il modulo in neutro.</span><span class="sxs-lookup"><span data-stu-id="77602-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="77602-116">Se nessuno dei passaggi precedenti ha esito positivo, il modulo non supporta la lingua richiesta e l'Unione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="77602-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



