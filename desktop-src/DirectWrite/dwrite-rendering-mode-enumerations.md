---
title: Enumerazioni di DWRITE_RENDERING_MODE
description: A partire da Windows 8, l' \_ enumerazione della modalità di rendering DWrite ha \_ aggiunto nuovi valori di enumerazione e ne è stato deprecato altri.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2019
ms.locfileid: "103955038"
---
# <a name="dwrite_rendering_mode-enumerations"></a><span data-ttu-id="f01ec-103">\_Enumerazioni della modalità di rendering DWrite \_</span><span class="sxs-lookup"><span data-stu-id="f01ec-103">DWRITE\_RENDERING\_MODE enumerations</span></span>

<span data-ttu-id="f01ec-104">A partire da Windows 8, l'enumerazione della **\_ \_ modalità di rendering DWrite** ha aggiunto nuovi valori di enumerazione e ne è stato deprecato altri.</span><span class="sxs-lookup"><span data-stu-id="f01ec-104">Starting in Windows 8, the **DWRITE\_RENDERING\_MODE** enumeration added new enumeration values and deprecated others.</span></span>

<span data-ttu-id="f01ec-105">A partire da Windows 8, l'enumerazione [**DWrite \_ Text \_ antialias \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) determina se il rendering del testo viene eseguito con ClearType.</span><span class="sxs-lookup"><span data-stu-id="f01ec-105">Starting in Windows 8, the [**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) enumeration determines whether text is rendered using ClearType.</span></span> <span data-ttu-id="f01ec-106">Di conseguenza, tutte le modalità di rendering ClearType nell'enumerazione **della \_ \_ modalità di rendering DWrite** sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="f01ec-106">As a result, all the ClearType rendering modes in the **DWRITE\_RENDERING\_MODE** enumeration are deprecated.</span></span> <span data-ttu-id="f01ec-107">Questi valori di enumerazione ora vengono mappati alle nuove modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="f01ec-107">These enumeration values now map to new rendering modes.</span></span>

<span data-ttu-id="f01ec-108">La tabella seguente mostra i valori di enumerazione precedenti e i nuovi valori a cui viene eseguito il mapping.</span><span class="sxs-lookup"><span data-stu-id="f01ec-108">The table here shows the old enumeration values and the new values they are mapped to.</span></span> <span data-ttu-id="f01ec-109">Per le descrizioni dei nuovi valori, vedere [**\_ \_ modalità di rendering DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span><span class="sxs-lookup"><span data-stu-id="f01ec-109">For descriptions of the new values, see [**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span></span>



| <span data-ttu-id="f01ec-110">Modalità precedente</span><span class="sxs-lookup"><span data-stu-id="f01ec-110">Old mode</span></span>                                                                                | <span data-ttu-id="f01ec-111">Nuova modalità</span><span class="sxs-lookup"><span data-stu-id="f01ec-111">New mode</span></span>                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f01ec-112">**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ GDI \_ classico**</span><span class="sxs-lookup"><span data-stu-id="f01ec-112">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="f01ec-113">**\_modalità di rendering DWrite \_ \_ GDI \_ classico**</span><span class="sxs-lookup"><span data-stu-id="f01ec-113">**DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="f01ec-114">**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ GDI \_ naturale**</span><span class="sxs-lookup"><span data-stu-id="f01ec-114">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="f01ec-115">**\_modalità di rendering DWrite \_ \_ GDI \_ Natural**</span><span class="sxs-lookup"><span data-stu-id="f01ec-115">**DWRITE\_RENDERING\_MODE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="f01ec-116">**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ naturale**</span><span class="sxs-lookup"><span data-stu-id="f01ec-116">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [<span data-ttu-id="f01ec-117">**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ naturale**</span><span class="sxs-lookup"><span data-stu-id="f01ec-117">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [<span data-ttu-id="f01ec-118">**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ naturale \_ simmetrica**</span><span class="sxs-lookup"><span data-stu-id="f01ec-118">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [<span data-ttu-id="f01ec-119">**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ naturale \_ simmetrica**</span><span class="sxs-lookup"><span data-stu-id="f01ec-119">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a><span data-ttu-id="f01ec-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f01ec-120">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f01ec-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="f01ec-121">Topic</span></span></th>
<th><span data-ttu-id="f01ec-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f01ec-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f01ec-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 e versioni successive)</strong></a></span><span class="sxs-lookup"><span data-stu-id="f01ec-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 and later)</strong></a></span></span><br/></td>
<td><span data-ttu-id="f01ec-124">Rappresenta un metodo di rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="f01ec-124">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f01ec-125">Questo argomento riguarda <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f01ec-125">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 and later.</span></span> <span data-ttu-id="f01ec-126">Per informazioni sulla versione precedente, vedere <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>questo argomento</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f01ec-126">For info on the previous version see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>this topic</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f01ec-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f01ec-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="f01ec-128">Rappresenta un metodo di rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="f01ec-128">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f01ec-129">Questo argomento riguarda <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> precedente a Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f01ec-129">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> previous to Windows 8 and later.</span></span> <span data-ttu-id="f01ec-130">Per informazioni sulla versione più recente, vedere <strong>questo argomento</strong>.</span><span class="sxs-lookup"><span data-stu-id="f01ec-130">For info on the newer version see <strong>this topic</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





