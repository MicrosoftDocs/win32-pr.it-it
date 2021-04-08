---
description: Costanti SMONTHNAME delle impostazioni locali \_ \*
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: Costanti LOCALE_SMONTHNAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752802"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="e4170-103">Costanti SMONTHNAME delle impostazioni locali \_ \*</span><span class="sxs-lookup"><span data-stu-id="e4170-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="e4170-104">Questo argomento definisce le impostazioni locali \_ SMONTHNAME \* costanti usate da NLS.</span><span class="sxs-lookup"><span data-stu-id="e4170-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4170-105">Valore</span><span class="sxs-lookup"><span data-stu-id="e4170-105">Value</span></span></th>
<th><span data-ttu-id="e4170-106">Significato</span><span class="sxs-lookup"><span data-stu-id="e4170-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4170-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="e4170-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="e4170-108">Nome lungo nativo per gennaio.</span><span class="sxs-lookup"><span data-stu-id="e4170-108">Native long name for January.</span></span> <span data-ttu-id="e4170-109">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4170-110">Chiamando la funzione <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> con una costante LOCALE_SMONTHNAME \* viene restituita la forma autonoma o candidativa del nome del mese.</span><span class="sxs-lookup"><span data-stu-id="e4170-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="e4170-111">Per ottenere il formato genitivo del nome del mese, l'applicazione chiama <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> o <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> con una data immagine di ddMMMM e rimuove le due cifre dall'inizio della stringa recuperata.</span><span class="sxs-lookup"><span data-stu-id="e4170-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="e4170-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="e4170-113">Nome lungo nativo per febbraio.</span><span class="sxs-lookup"><span data-stu-id="e4170-113">Native long name for February.</span></span> <span data-ttu-id="e4170-114">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-115">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="e4170-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="e4170-117">Nome lungo nativo per marzo.</span><span class="sxs-lookup"><span data-stu-id="e4170-117">Native long name for March.</span></span> <span data-ttu-id="e4170-118">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-119">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="e4170-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="e4170-121">Nome lungo nativo per aprile.</span><span class="sxs-lookup"><span data-stu-id="e4170-121">Native long name for April.</span></span> <span data-ttu-id="e4170-122">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-123">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="e4170-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="e4170-125">Nome lungo nativo per May.</span><span class="sxs-lookup"><span data-stu-id="e4170-125">Native long name for May.</span></span> <span data-ttu-id="e4170-126">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-127">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="e4170-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="e4170-129">Nome lungo nativo per giugno.</span><span class="sxs-lookup"><span data-stu-id="e4170-129">Native long name for June.</span></span> <span data-ttu-id="e4170-130">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-131">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="e4170-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="e4170-133">Nome lungo nativo per luglio.</span><span class="sxs-lookup"><span data-stu-id="e4170-133">Native long name for July.</span></span> <span data-ttu-id="e4170-134">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-135">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="e4170-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="e4170-137">Nome lungo nativo per agosto.</span><span class="sxs-lookup"><span data-stu-id="e4170-137">Native long name for August.</span></span> <span data-ttu-id="e4170-138">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-139">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="e4170-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="e4170-141">Nome lungo nativo per settembre.</span><span class="sxs-lookup"><span data-stu-id="e4170-141">Native long name for September.</span></span> <span data-ttu-id="e4170-142">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-143">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="e4170-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="e4170-145">Nome lungo nativo per ottobre.</span><span class="sxs-lookup"><span data-stu-id="e4170-145">Native long name for October.</span></span> <span data-ttu-id="e4170-146">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-147">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="e4170-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="e4170-149">Nome lungo nativo per novembre.</span><span class="sxs-lookup"><span data-stu-id="e4170-149">Native long name for November.</span></span> <span data-ttu-id="e4170-150">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-151">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4170-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="e4170-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="e4170-153">Nome lungo nativo per dicembre.</span><span class="sxs-lookup"><span data-stu-id="e4170-153">Native long name for December.</span></span> <span data-ttu-id="e4170-154">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-155">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4170-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="e4170-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="e4170-157">Nome nativo per un tredicesimo mese, se esistente.</span><span class="sxs-lookup"><span data-stu-id="e4170-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="e4170-158">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="e4170-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4170-159">Per LOCALE_SMONTHNAME1, vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="e4170-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




