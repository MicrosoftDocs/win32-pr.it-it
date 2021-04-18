---
title: Attributo di stampa la
description: Attributo di stampa la
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299900"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="326ee-103">Attributo di stampa la</span><span class="sxs-lookup"><span data-stu-id="326ee-103">VML Print Attribute</span></span>

<span data-ttu-id="326ee-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="326ee-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="326ee-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="326ee-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="326ee-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="326ee-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="326ee-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="326ee-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="326ee-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="326ee-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="326ee-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="326ee-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="326ee-110">Determina se la forma verrà stampata.</span><span class="sxs-lookup"><span data-stu-id="326ee-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="326ee-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="326ee-111">Read/write.</span></span> <span data-ttu-id="326ee-112">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="326ee-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="326ee-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="326ee-113">**Applies To**</span></span>

[<span data-ttu-id="326ee-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="326ee-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="326ee-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="326ee-115">**Tag Syntax**</span></span>

<span data-ttu-id="326ee-116"><v: *element* Print = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="326ee-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="326ee-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="326ee-117">**Script Syntax**</span></span>

<span data-ttu-id="326ee-118">*element* . Print = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="326ee-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="326ee-119">*espressione* = *elemento*. Print</span><span class="sxs-lookup"><span data-stu-id="326ee-119">*expression*=*element*.print</span></span>

<span data-ttu-id="326ee-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="326ee-120">**Remarks**</span></span>

<span data-ttu-id="326ee-121">Fornito come metodo per specificare se verranno stampate forme.</span><span class="sxs-lookup"><span data-stu-id="326ee-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="326ee-122">Si noti che è comunque possibile visualizzare una forma sullo schermo, anche se non viene stampata come risultato di questo attributo **false**.</span><span class="sxs-lookup"><span data-stu-id="326ee-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="326ee-123">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="326ee-123">The default value is **True**.</span></span>

<span data-ttu-id="326ee-124">Questo attributo viene utilizzato da Microsoft Office ma non viene utilizzato da Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="326ee-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="326ee-125">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="326ee-125">*Microsoft Office Extensions Attribute*</span></span>

 

 