---
title: Attributo TableProperties di la
description: Attributo TableProperties di la
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299846"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="690f7-103">Attributo TableProperties di la</span><span class="sxs-lookup"><span data-stu-id="690f7-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="690f7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="690f7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="690f7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="690f7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="690f7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="690f7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="690f7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="690f7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="690f7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="690f7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="690f7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="690f7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="690f7-110">Determina le proprietà della tabella.</span><span class="sxs-lookup"><span data-stu-id="690f7-110">Determines table properties.</span></span> <span data-ttu-id="690f7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="690f7-111">Read/write.</span></span> <span data-ttu-id="690f7-112">**Integer**.</span><span class="sxs-lookup"><span data-stu-id="690f7-112">**Integer**.</span></span>

<span data-ttu-id="690f7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="690f7-113">**Applies To**</span></span>

[<span data-ttu-id="690f7-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="690f7-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="690f7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="690f7-115">**Tag Syntax**</span></span>

<span data-ttu-id="690f7-116"><v: *element* o:tableProperties = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="690f7-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="690f7-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="690f7-117">**Remarks**</span></span>

<span data-ttu-id="690f7-118">Usato da Microsoft PowerPoint per le tabelle native.</span><span class="sxs-lookup"><span data-stu-id="690f7-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="690f7-119">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="690f7-119">Default value is 0.</span></span> <span data-ttu-id="690f7-120">Vengono utilizzati solo i primi tre bit di questo Integer.</span><span class="sxs-lookup"><span data-stu-id="690f7-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="690f7-121">Anche se il valore viene archiviato in una forma, l'attributo è utile solo quando la tabella è costituita da forme raggruppate. È possibile combinare BITS.</span><span class="sxs-lookup"><span data-stu-id="690f7-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="690f7-122">Sono inclusi i seguenti valori di bit.</span><span class="sxs-lookup"><span data-stu-id="690f7-122">The following bit values are included.</span></span>



| <span data-ttu-id="690f7-123">bit</span><span class="sxs-lookup"><span data-stu-id="690f7-123">Bit</span></span> | <span data-ttu-id="690f7-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="690f7-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="690f7-125">1</span><span class="sxs-lookup"><span data-stu-id="690f7-125">1</span></span>   | <span data-ttu-id="690f7-126">Impostare se il gruppo di forme è una tabella.</span><span class="sxs-lookup"><span data-stu-id="690f7-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="690f7-127">2</span><span class="sxs-lookup"><span data-stu-id="690f7-127">2</span></span>   | <span data-ttu-id="690f7-128">Impostare se la forma è un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="690f7-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="690f7-129">3</span><span class="sxs-lookup"><span data-stu-id="690f7-129">3</span></span>   | <span data-ttu-id="690f7-130">Impostare se il testo della tabella è bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="690f7-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="690f7-131">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="690f7-131">*Microsoft Office Extensions Attribute*</span></span>

 

 