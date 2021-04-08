---
description: Descrive i formati di data supportati per l'utilizzo nella clausola WHERE di WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formati di data WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882297"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="afabc-103">Formati di data WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="afabc-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="afabc-104">Oltre al formato **DateTime** WMI, i formati di data seguenti sono supportati per l'utilizzo nella clausola **where** di WQL.</span><span class="sxs-lookup"><span data-stu-id="afabc-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="afabc-105">Il formato di ora visualizzato è diverso per le diverse impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="afabc-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="afabc-106">Gli script che si connettono ai computer remoti devono specificare l'ora nel formato appropriato per le impostazioni locali del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afabc-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="afabc-107">Ad esempio, il formato di data e ora Stati Uniti è MM-gg-aaaa.</span><span class="sxs-lookup"><span data-stu-id="afabc-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="afabc-108">Se uno script in un computer usa si connette a un computer di destinazione in impostazioni locali in cui il formato è GG-MM-AAAA, le query vengono elaborate nel computer di destinazione come GG-MM-AAAA.</span><span class="sxs-lookup"><span data-stu-id="afabc-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="afabc-109">Per evitare risultati diversi tra le impostazioni locali, utilizzare il formato [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="afabc-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="afabc-110">Per altre informazioni, vedere [formato di data e ora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="afabc-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="afabc-111">Formato</span><span class="sxs-lookup"><span data-stu-id="afabc-111">Format</span></span></th>
<th><span data-ttu-id="afabc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afabc-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="afabc-113">Lun [TH] dd [,] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="afabc-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="afabc-114">Mese (digitato o abbreviato in tre lettere), giorno, virgola facoltativa e anno a due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="afabc-115">21 gennaio 1932</span><span class="sxs-lookup"><span data-stu-id="afabc-115">January 21, 1932</span></span><br />
<span data-ttu-id="afabc-116">21 gennaio 32</span><span class="sxs-lookup"><span data-stu-id="afabc-116">January 21, 32</span></span><br />
<span data-ttu-id="afabc-117">Gennaio 21 1932</span><span class="sxs-lookup"><span data-stu-id="afabc-117">Jan 21 1932</span></span><br />
<span data-ttu-id="afabc-118">Gennaio 21 32</span><span class="sxs-lookup"><span data-stu-id="afabc-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-119">Lun [TH] [,] aaaa</span><span class="sxs-lookup"><span data-stu-id="afabc-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="afabc-120">Mese (ortografico o abbreviato in tre lettere), virgola facoltativa e anno a quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="afabc-121">1932 gennaio</span><span class="sxs-lookup"><span data-stu-id="afabc-121">January 1932</span></span><br />
<span data-ttu-id="afabc-122">Gennaio 1932</span><span class="sxs-lookup"><span data-stu-id="afabc-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-123">Lun [TH] [AA] aa gg</span><span class="sxs-lookup"><span data-stu-id="afabc-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="afabc-124">Mese (ortografico o abbreviato in tre lettere), anno a due o quattro cifre e giorno.</span><span class="sxs-lookup"><span data-stu-id="afabc-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="afabc-125">1932 21 gennaio</span><span class="sxs-lookup"><span data-stu-id="afabc-125">January 1932 21</span></span><br />
<span data-ttu-id="afabc-126">Gennaio 32 21</span><span class="sxs-lookup"><span data-stu-id="afabc-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-127">DD Mon [TH] [,] [] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="afabc-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="afabc-128">Giorno del mese, mese (ortografico o abbreviato in tre lettere), virgola facoltativa, spazio facoltativo e anno a due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="afabc-129">21 gennaio, 1932</span><span class="sxs-lookup"><span data-stu-id="afabc-129">21 January, 1932</span></span><br />
<span data-ttu-id="afabc-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="afabc-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-131">DD [YY] YY lun [TH]</span><span class="sxs-lookup"><span data-stu-id="afabc-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="afabc-132">Giorno del mese, anno a due o quattro cifre e mese (digitato o abbreviato in tre lettere).</span><span class="sxs-lookup"><span data-stu-id="afabc-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="afabc-133">21 1932 gennaio</span><span class="sxs-lookup"><span data-stu-id="afabc-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-134">[YY] AA lun [TH] dd</span><span class="sxs-lookup"><span data-stu-id="afabc-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="afabc-135">Anno a due o quattro cifre, ovvero con ortografia o abbreviazione in tre lettere, e giorno.</span><span class="sxs-lookup"><span data-stu-id="afabc-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="afabc-136">1932 gennaio 21</span><span class="sxs-lookup"><span data-stu-id="afabc-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-137">aaaa lun [TH]</span><span class="sxs-lookup"><span data-stu-id="afabc-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="afabc-138">Anno e mese a due o quattro cifre (digitato o abbreviato in tre lettere).</span><span class="sxs-lookup"><span data-stu-id="afabc-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="afabc-139">1932 gen</span><span class="sxs-lookup"><span data-stu-id="afabc-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-140">aaaa gg Mon [TH]</span><span class="sxs-lookup"><span data-stu-id="afabc-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="afabc-141">Anno, giorno e mese a due o quattro cifre (digitato o abbreviato in tre lettere).</span><span class="sxs-lookup"><span data-stu-id="afabc-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="afabc-142">1932 21 gennaio</span><span class="sxs-lookup"><span data-stu-id="afabc-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-143">M M {/-.} gg {/-.} [YY] AA</span><span class="sxs-lookup"><span data-stu-id="afabc-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="afabc-144">Anno, mese, giorno e due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="afabc-145">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-146">gg {/-.} M M {/-.} [YY] AA</span><span class="sxs-lookup"><span data-stu-id="afabc-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="afabc-147">Giorno del mese, mese e anno a due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="afabc-148">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-149">M M {/-.} [YY] AA {/-.} GG</span><span class="sxs-lookup"><span data-stu-id="afabc-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="afabc-150">Mese, anno a due o quattro cifre e giorno.</span><span class="sxs-lookup"><span data-stu-id="afabc-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="afabc-151">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-152">gg {/-.} [YY] AA {/-.} M M</span><span class="sxs-lookup"><span data-stu-id="afabc-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="afabc-153">Giorno del mese, anno a due o quattro cifre e mese.</span><span class="sxs-lookup"><span data-stu-id="afabc-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="afabc-154">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-155">[YY] AA {/-.} gg {/-.} M M</span><span class="sxs-lookup"><span data-stu-id="afabc-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="afabc-156">Anno, giorno e mese di due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="afabc-157">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-158">[YY] AA {/-.} M M {/-.} GG</span><span class="sxs-lookup"><span data-stu-id="afabc-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="afabc-159">Anno, mese e giorno a due o quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="afabc-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="afabc-160">Si noti che i separatori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="afabc-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afabc-161">[AA] AAMMGG</span><span class="sxs-lookup"><span data-stu-id="afabc-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="afabc-162">Anno, mese e giorno con due o quattro cifre senza spazi.</span><span class="sxs-lookup"><span data-stu-id="afabc-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afabc-163">aaaa [MM [gg]]</span><span class="sxs-lookup"><span data-stu-id="afabc-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="afabc-164">Anno a due o quattro cifre, mese facoltativo e giorno facoltativo, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="afabc-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="afabc-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afabc-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afabc-166">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="afabc-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




