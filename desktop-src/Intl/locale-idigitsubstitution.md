---
description: impostazioni locali \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128118"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="f99f8-103">impostazioni locali \_ IDIGITSUBSTITUTION</span><span class="sxs-lookup"><span data-stu-id="f99f8-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="f99f8-104">**Windows 2000:** Forma delle cifre.</span><span class="sxs-lookup"><span data-stu-id="f99f8-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="f99f8-105">Ad esempio, le cifre arabe, tailandesi e indiane hanno forme classiche diverse dalle cifre europee.</span><span class="sxs-lookup"><span data-stu-id="f99f8-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="f99f8-106">Per le impostazioni locali con [ \_ SNATIVEDIGITS delle impostazioni locali](locale-snative-constants.md) specificate come valori diversi da ASCII 0-9, questo valore specifica se è necessario assegnare la preferenza a tali cifre a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f99f8-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="f99f8-107">Se, ad esempio, si sceglie un valore pari a 2, vengono sempre utilizzate le cifre specificate dalle impostazioni locali \_ SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="f99f8-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="f99f8-108">Se si sceglie 1, vengono sempre utilizzate le cifre ASCII 0-9.</span><span class="sxs-lookup"><span data-stu-id="f99f8-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="f99f8-109">Se si sceglie 0, viene usato ASCII in alcune circostanze e le cifre specificate dalle impostazioni locali \_ SNATIVEDIGITS vengono usate in altre, a seconda del contesto.</span><span class="sxs-lookup"><span data-stu-id="f99f8-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f99f8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f99f8-110">Value</span></span></th>
<th><span data-ttu-id="f99f8-111">Significato</span><span class="sxs-lookup"><span data-stu-id="f99f8-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f99f8-112">0</span><span class="sxs-lookup"><span data-stu-id="f99f8-112">0</span></span></td>
<td><span data-ttu-id="f99f8-113">Sostituzione basata sul contesto.</span><span class="sxs-lookup"><span data-stu-id="f99f8-113">Context-based substitution.</span></span> <span data-ttu-id="f99f8-114">Le cifre vengono visualizzate in base al testo precedente nello stesso output.</span><span class="sxs-lookup"><span data-stu-id="f99f8-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="f99f8-115">Le cifre europee seguono gli alfabeti latini, Arabic-Indic cifre seguono il testo arabo e altre cifre nazionali seguono il testo scritto in diversi altri script.</span><span class="sxs-lookup"><span data-stu-id="f99f8-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="f99f8-116">Quando non è presente un testo precedente, le impostazioni locali e l'ordine di lettura visualizzato determinano la sostituzione dei numeri, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f99f8-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f99f8-117">Locale</span><span class="sxs-lookup"><span data-stu-id="f99f8-117">Locale</span></span></th>
<th><span data-ttu-id="f99f8-118">Ordine di lettura</span><span class="sxs-lookup"><span data-stu-id="f99f8-118">Reading order</span></span></th>
<th><span data-ttu-id="f99f8-119">Cifre utilizzate</span><span class="sxs-lookup"><span data-stu-id="f99f8-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f99f8-120">Arabo</span><span class="sxs-lookup"><span data-stu-id="f99f8-120">Arabic</span></span></td>
<td><span data-ttu-id="f99f8-121">Da destra a sinistra</span><span class="sxs-lookup"><span data-stu-id="f99f8-121">Right-to-left</span></span></td>
<td><span data-ttu-id="f99f8-122">Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="f99f8-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f99f8-123">Thai</span><span class="sxs-lookup"><span data-stu-id="f99f8-123">Thai</span></span></td>
<td><span data-ttu-id="f99f8-124">Da sinistra a destra</span><span class="sxs-lookup"><span data-stu-id="f99f8-124">Left-to-right</span></span></td>
<td><span data-ttu-id="f99f8-125">Cifre tailandesi</span><span class="sxs-lookup"><span data-stu-id="f99f8-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f99f8-126">Tutti gli altri</span><span class="sxs-lookup"><span data-stu-id="f99f8-126">All others</span></span></td>
<td><span data-ttu-id="f99f8-127">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="f99f8-127">Any</span></span></td>
<td><span data-ttu-id="f99f8-128">Nessuna sostituzione utilizzata</span><span class="sxs-lookup"><span data-stu-id="f99f8-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f99f8-129">1</span><span class="sxs-lookup"><span data-stu-id="f99f8-129">1</span></span></td>
<td><span data-ttu-id="f99f8-130">Nessuna sostituzione utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f99f8-130">No substitution used.</span></span> <span data-ttu-id="f99f8-131">Compatibilità completa con Unicode.</span><span class="sxs-lookup"><span data-stu-id="f99f8-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f99f8-132">2</span><span class="sxs-lookup"><span data-stu-id="f99f8-132">2</span></span></td>
<td><span data-ttu-id="f99f8-133">Sostituzione delle cifre native.</span><span class="sxs-lookup"><span data-stu-id="f99f8-133">Native digit substitution.</span></span> <span data-ttu-id="f99f8-134">Le forme nazionali vengono visualizzate in base LOCALE_SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="f99f8-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



