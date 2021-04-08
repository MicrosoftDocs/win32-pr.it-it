---
title: Attributo Matrix (asimmetria) (la)
description: Attributo Matrix (asimmetria) (la)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047268"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="98227-103">Attributo Matrix (asimmetria) (la)</span><span class="sxs-lookup"><span data-stu-id="98227-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="98227-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="98227-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="98227-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="98227-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="98227-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="98227-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="98227-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="98227-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="98227-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="98227-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="98227-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="98227-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="98227-110">Definisce una trasformazione della prospettiva di una asimmetria.</span><span class="sxs-lookup"><span data-stu-id="98227-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="98227-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="98227-111">Read/write.</span></span> <span data-ttu-id="98227-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="98227-112">**String**.</span></span>

<span data-ttu-id="98227-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="98227-113">**Applies To**</span></span>

[<span data-ttu-id="98227-114">Sfasamento</span><span class="sxs-lookup"><span data-stu-id="98227-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="98227-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="98227-115">**Tag Syntax**</span></span>

<span data-ttu-id="98227-116"><o: *element* Matrix = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="98227-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="98227-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="98227-117">**Script Syntax**</span></span>

<span data-ttu-id="98227-118">*element* . Matrix = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="98227-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="98227-119">*espressione* = *element*. Matrix</span><span class="sxs-lookup"><span data-stu-id="98227-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="98227-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="98227-120">**Remarks**</span></span>

<span data-ttu-id="98227-121">La matrice è una stringa nel formato "SXX, SXY, SYX, SYY, px, py", dove s è scale, p è Perspective e x e y sono valori x e y.</span><span class="sxs-lookup"><span data-stu-id="98227-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="98227-122">Se l' [offset](offset-attribute--skew--vml.md) è espresso in unità assolute, px e py si trovano nelle [unità](msdn-online-vml-units.md) Emu ^-1 (in caso contrario si tratta di una frazione inversa della dimensione della forma).</span><span class="sxs-lookup"><span data-stu-id="98227-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="98227-123">Il valore predefinito è "1, 0, 0, 1, 0, 0".</span><span class="sxs-lookup"><span data-stu-id="98227-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="98227-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="98227-124">*Microsoft Office Extensions Attribute*</span></span>

 

 