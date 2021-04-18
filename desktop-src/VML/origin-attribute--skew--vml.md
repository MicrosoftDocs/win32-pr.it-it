---
title: Attributo Origin (asimmetria) (la)
description: Attributo Origin (asimmetria) (la)
ms.assetid: 36f77073-7438-41b3-9107-95e27b01b776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0c134ad8e7000e71a4237a6b5aac80e874c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399676"
---
# <a name="origin-attribute-skewvml"></a><span data-ttu-id="b099f-103">Attributo Origin (asimmetria) (la)</span><span class="sxs-lookup"><span data-stu-id="b099f-103">Origin Attribute (Skew)(VML)</span></span>

<span data-ttu-id="b099f-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b099f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b099f-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b099f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b099f-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b099f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b099f-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b099f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b099f-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b099f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b099f-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b099f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b099f-110">Definisce l'origine dell'asimmetria.</span><span class="sxs-lookup"><span data-stu-id="b099f-110">Defines the origin of the skew.</span></span> <span data-ttu-id="b099f-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b099f-111">Read/write.</span></span> <span data-ttu-id="b099f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b099f-112">**VgVector2D**.</span></span>

<span data-ttu-id="b099f-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b099f-113">**Applies To**</span></span>

[<span data-ttu-id="b099f-114">Sfasamento</span><span class="sxs-lookup"><span data-stu-id="b099f-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="b099f-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b099f-115">**Tag Syntax**</span></span>

<span data-ttu-id="b099f-116"><o: *element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b099f-116"><o: *element* origin=" *expression* "></span></span>

<span data-ttu-id="b099f-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b099f-117">**Script Syntax**</span></span>

<span data-ttu-id="b099f-118">*element* . Origin = "*espressione \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="b099f-118">*element* .origin="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="b099f-119">*espressione* = *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="b099f-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="b099f-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b099f-120">**Remarks**</span></span>

<span data-ttu-id="b099f-121">I valori sono in genere una percentuale delle dimensioni della forma e variano da-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="b099f-121">Values are typically a percentage of the shape's size and range from -0.5 to +0.5.</span></span> <span data-ttu-id="b099f-122">Sono consentiti valori maggiori che assegnano offset come multipli della dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="b099f-122">Larger values are allowed that give offsets as multiples of the shape's size.</span></span> <span data-ttu-id="b099f-123">Il valore predefinito è 0, 0.</span><span class="sxs-lookup"><span data-stu-id="b099f-123">The default is 0,0.</span></span>

<span data-ttu-id="b099f-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="b099f-124">*Microsoft Office Extensions Attribute*</span></span>

 

 