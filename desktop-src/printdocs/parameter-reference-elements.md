---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementi ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058484"
---
# <a name="parameterref-elements"></a><span data-ttu-id="fc4ae-104">Elementi ParameterRef</span><span class="sxs-lookup"><span data-stu-id="fc4ae-104">ParameterRef Elements</span></span>

<span data-ttu-id="fc4ae-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-105">This topic is not current.</span></span> <span data-ttu-id="fc4ae-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fc4ae-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc4ae-107">Gli elementi ParameterRef si applicano in modo specifico agli elementi option, consentendo a tale elemento option di fare riferimento a un particolare elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-107">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="fc4ae-108">Per questi elementi di opzioni, un elemento ScoredProperty che caratterizza l'opzione non è hardcoded nel documento PrintCapabilities come valore, ma è invece una variabile.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-108">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="fc4ae-109">Per abilitare questa variabilità, questi elementi ScoredProperty contengono un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-109">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="fc4ae-110">Un elemento ScoredProperty non può contenere sia un elemento Value che un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-110">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="fc4ae-111">Gli elementi option che contengono uno o più elementi ParameterRef sono denominati elementi option con parametri.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-111">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="fc4ae-112">Print Schema Framework consente a un elemento option di contenere un numero qualsiasi di elementi ScoredProperty che fanno riferimento a elementi Parameter, insieme a un numero qualsiasi di elementi ScoredProperty che contengono elementi di valore.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-112">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="fc4ae-113">Il Framework consente inoltre a qualsiasi numero di elementi di funzionalità di contenere elementi di opzioni con parametri e un numero qualsiasi di elementi di opzioni con parametri è consentito per ogni elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-113">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="fc4ae-114">Inoltre, è possibile fare riferimento allo stesso costrutto di parametro da più elementi option diversi, elementi option che possono appartenere allo stesso o a elementi di funzionalità diversi.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-114">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc4ae-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc4ae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc4ae-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fc4ae-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



