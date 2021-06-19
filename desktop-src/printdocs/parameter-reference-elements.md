---
description: Leggere gli elementi ParameterRef in Print Schema Framework. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementi ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396526"
---
# <a name="parameterref-elements"></a><span data-ttu-id="81e81-105">Elementi ParameterRef</span><span class="sxs-lookup"><span data-stu-id="81e81-105">ParameterRef Elements</span></span>

<span data-ttu-id="81e81-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="81e81-106">This topic is not current.</span></span> <span data-ttu-id="81e81-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="81e81-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="81e81-108">Gli elementi ParameterRef si applicano in modo specifico agli elementi Option, consentendo a tale elemento Option di fare riferimento a un particolare elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="81e81-108">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="81e81-109">Per questi elementi Option, un elemento ScoredProperty che caratterizza l'opzione non è hard-coded nel documento PrintCapabilities come valore, ma è variabile.</span><span class="sxs-lookup"><span data-stu-id="81e81-109">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="81e81-110">Per abilitare questa variabilità, questi elementi ScoredProperty contengono un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="81e81-110">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="81e81-111">Un elemento ScoredProperty non può contenere sia un elemento Value che un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="81e81-111">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="81e81-112">Gli elementi opzione contenenti uno o più elementi ParameterRef sono denominati elementi Option con parametri.</span><span class="sxs-lookup"><span data-stu-id="81e81-112">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="81e81-113">Print Schema Framework consente a un elemento Option di contenere un numero qualsiasi di elementi ScoredProperty che fanno riferimento agli elementi Parameter, insieme a qualsiasi numero di elementi ScoredProperty che contengono elementi Value.</span><span class="sxs-lookup"><span data-stu-id="81e81-113">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="81e81-114">Framework consente anche a qualsiasi numero di elementi Feature di contenere elementi Option con parametri e a ogni elemento Feature è consentito un numero qualsiasi di elementi Option con parametri.</span><span class="sxs-lookup"><span data-stu-id="81e81-114">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="81e81-115">Inoltre, lo stesso costrutto di parametro può essere indicato da diversi elementi Option, elementi Option che possono appartenere allo stesso elemento Feature o a elementi Feature diversi.</span><span class="sxs-lookup"><span data-stu-id="81e81-115">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81e81-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81e81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81e81-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="81e81-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



