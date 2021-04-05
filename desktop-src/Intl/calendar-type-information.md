---
description: In questo argomento vengono descritte le informazioni sul tipo di calendario (tipo di dati CALTYPE) utilizzate nelle funzioni EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo e GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informazioni sul tipo di calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884590"
---
# <a name="calendar-type-information"></a><span data-ttu-id="df5ae-103">Informazioni sul tipo di calendario</span><span class="sxs-lookup"><span data-stu-id="df5ae-103">Calendar Type Information</span></span>

<span data-ttu-id="df5ae-104">In questo argomento vengono descritte le informazioni sul tipo di calendario (tipo di dati CALTYPE) utilizzate nelle funzioni [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)e [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="df5ae-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="df5ae-105">Alcuni di questi valori vengono usati anche dalla funzione [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="df5ae-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="df5ae-106">Le costanti CALTYPE seguenti possono essere utilizzate in combinazione con qualsiasi altra costante di CALTYPE.</span><span class="sxs-lookup"><span data-stu-id="df5ae-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="df5ae-107">Costante</span><span class="sxs-lookup"><span data-stu-id="df5ae-107">Constant</span></span>                     | <span data-ttu-id="df5ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df5ae-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df5ae-109">\_NOUSEROVERRIDE Cal</span><span class="sxs-lookup"><span data-stu-id="df5ae-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="df5ae-110">**Windows Me/98, windows 2000:** Utilizzare l'impostazione predefinita del sistema anziché la scelta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df5ae-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="df5ae-111">\_ \_ nomi dei genitivi restituiti da Cal \_</span><span class="sxs-lookup"><span data-stu-id="df5ae-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="df5ae-112">**Windows 7 e versioni successive:** Recuperare il risultato da [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) nel formato dei nomi di genial of months, ovvero i nomi usati quando i nomi dei mesi vengono combinati con altri elementi.</span><span class="sxs-lookup"><span data-stu-id="df5ae-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="df5ae-113">Ad esempio, in ucraino l'equivalente di gennaio viene scritto come "Січень" quando il mese è denominato da solo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="df5ae-114">Tuttavia, quando il nome del mese viene usato in combinazione, ad esempio, in una data, ad esempio il 5 gennaio 2003, viene usata la forma genitiva del nome.</span><span class="sxs-lookup"><span data-stu-id="df5ae-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="df5ae-115">Per l'esempio ucraino, il nome del mese del genico viene visualizzato come "5 січня 2003".</span><span class="sxs-lookup"><span data-stu-id="df5ae-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="df5ae-116">Per ulteriori informazioni, vedere la pagina relativa alle [impostazioni locali \_ restituiscono \_ \_ nomi di genitivi](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="df5ae-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="df5ae-117">\_numero restituito \_ Cal</span><span class="sxs-lookup"><span data-stu-id="df5ae-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="df5ae-118">**Windows Me/98, windows 2000:** Recuperare il risultato da [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) come numero anziché come stringa.</span><span class="sxs-lookup"><span data-stu-id="df5ae-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="df5ae-119">Questa operazione è valida solo per i valori che iniziano con CAL \_ I.</span><span class="sxs-lookup"><span data-stu-id="df5ae-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="df5ae-120">CAL \_ usare \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="df5ae-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="df5ae-121">**Windows Me/98, windows 2000:** Usare la tabella codici ANSI di sistema (ACP) invece della tabella codici delle impostazioni locali per la conversione di stringhe.</span><span class="sxs-lookup"><span data-stu-id="df5ae-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="df5ae-122">Questa operazione è rilevante solo per le versioni ANSI delle funzioni, ad esempio **EnumCalendarInfoA**.</span><span class="sxs-lookup"><span data-stu-id="df5ae-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="df5ae-123">Le costanti CALTYPE seguenti si escludono reciprocamente e non possono essere usate in combinazione tra loro in una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="df5ae-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df5ae-124">Costante</span><span class="sxs-lookup"><span data-stu-id="df5ae-124">Constant</span></span></th>
<th><span data-ttu-id="df5ae-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df5ae-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df5ae-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="df5ae-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="df5ae-127">Valore integer che indica il tipo di calendario del calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="df5ae-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="df5ae-129"><strong>Windows Me/98, windows 2000:</strong> Valore intero che indica il limite superiore dell'intervallo dell'anno a due cifre.</span><span class="sxs-lookup"><span data-stu-id="df5ae-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="df5ae-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="df5ae-131">Una o più stringhe con terminazione null che specificano gli offset dell'anno per ogni intervallo di era.</span><span class="sxs-lookup"><span data-stu-id="df5ae-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="df5ae-132">L'ultima stringa ha un carattere null di terminazione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="df5ae-133">Questo valore varia in formato a seconda del tipo di calendario facoltativo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="df5ae-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="df5ae-135">Nome nativo abbreviato del primo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="df5ae-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="df5ae-137">Nome nativo abbreviato del secondo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="df5ae-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="df5ae-139">Nome nativo abbreviato del terzo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="df5ae-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="df5ae-141">Nome nativo abbreviato del quarto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="df5ae-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="df5ae-143">Nome nativo abbreviato del quinto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="df5ae-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="df5ae-145">Nome nativo abbreviato del sesto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="df5ae-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="df5ae-147">Nome nativo abbreviato del settimo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="df5ae-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="df5ae-149"><strong>Windows 7 e versioni successive:</strong> Nome nativo abbreviato di un'era.</span><span class="sxs-lookup"><span data-stu-id="df5ae-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="df5ae-150">L'intera era rappresentata dalla costante CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="df5ae-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="df5ae-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="df5ae-152">Nome nativo abbreviato del primo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="df5ae-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="df5ae-154">Nome nativo abbreviato del secondo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="df5ae-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="df5ae-156">Nome nativo abbreviato del terzo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="df5ae-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="df5ae-158">Nome nativo abbreviato del quarto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="df5ae-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="df5ae-160">Nome nativo abbreviato del quinto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="df5ae-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="df5ae-162">Nome nativo abbreviato del sesto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="df5ae-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="df5ae-164">Nome nativo abbreviato del settimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="df5ae-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="df5ae-166">Nome nativo abbreviato dell'ottavo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="df5ae-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="df5ae-168">Nome nativo abbreviato del nono mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="df5ae-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="df5ae-170">Nome nativo abbreviato del decimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="df5ae-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="df5ae-172">Nome nativo abbreviato dell'undicesimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="df5ae-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="df5ae-174">Nome nativo abbreviato del dodicesimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="df5ae-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="df5ae-176">Nome nativo abbreviato del tredicesimo mese dell'anno, se esistente.</span><span class="sxs-lookup"><span data-stu-id="df5ae-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="df5ae-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="df5ae-178">Nome nativo del calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="df5ae-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="df5ae-180">Nome nativo del primo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="df5ae-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="df5ae-182">Nome nativo del secondo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="df5ae-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="df5ae-184">Nome nativo del terzo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="df5ae-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="df5ae-186">Nome nativo del quarto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="df5ae-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="df5ae-188">Nome nativo del quinto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="df5ae-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="df5ae-190">Nome nativo del sesto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="df5ae-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="df5ae-192">Nome nativo del settimo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="df5ae-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="df5ae-194">Una o più stringhe con terminazione null che specificano ognuno dei punti di codice Unicode che specificano l'era associata a CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="df5ae-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="df5ae-195">L'ultima stringa ha un carattere null di terminazione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="df5ae-196">Questo valore varia in formato a seconda del tipo di calendario facoltativo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="df5ae-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="df5ae-198">Formati di data estesa per il tipo di calendario.</span><span class="sxs-lookup"><span data-stu-id="df5ae-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="df5ae-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="df5ae-200"><strong>Windows 7 e versioni successive:</strong> Formato del mese e del giorno per il tipo di calendario.</span><span class="sxs-lookup"><span data-stu-id="df5ae-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="df5ae-201">La formattazione è simile a quella per CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="df5ae-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="df5ae-202">Ad esempio, se il modello mese/giorno è il nome completo del mese seguito dal numero di giorno con zeri iniziali, ad esempio il &quot; 03 settembre &quot; , il formato è &quot; MMMM dd &quot; .</span><span class="sxs-lookup"><span data-stu-id="df5ae-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="df5ae-203">È possibile utilizzare le virgolette singole per inserire caratteri non di formato, ad esempio, "de" in spagnolo.</span><span class="sxs-lookup"><span data-stu-id="df5ae-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="df5ae-204">Questo tipo di calendario supporta un solo formato.</span><span class="sxs-lookup"><span data-stu-id="df5ae-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="df5ae-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="df5ae-206">Nome nativo del primo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="df5ae-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="df5ae-208">Nome nativo del secondo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="df5ae-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="df5ae-210">Nome nativo del terzo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="df5ae-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="df5ae-212">Nome nativo del quarto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="df5ae-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="df5ae-214">Nome nativo del quinto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="df5ae-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="df5ae-216">Nome nativo del sesto mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="df5ae-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="df5ae-218">Nome nativo del settimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="df5ae-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="df5ae-220">Nome nativo dell'ottavo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="df5ae-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="df5ae-222">Nome nativo del nono mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="df5ae-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="df5ae-224">Nome nativo del decimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="df5ae-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="df5ae-226">Nome nativo dell'undicesimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="df5ae-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="df5ae-228">Nome nativo del dodicesimo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="df5ae-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="df5ae-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="df5ae-230">Nome nativo del tredicesimo mese dell'anno, se esistente.</span><span class="sxs-lookup"><span data-stu-id="df5ae-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="df5ae-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="df5ae-232">Formati di data breve per il tipo di calendario.</span><span class="sxs-lookup"><span data-stu-id="df5ae-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="df5ae-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="df5ae-234"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del primo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="df5ae-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="df5ae-236"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del secondo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="df5ae-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="df5ae-238"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del terzo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="df5ae-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="df5ae-240"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del quarto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="df5ae-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="df5ae-242"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del quinto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="df5ae-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="df5ae-244"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del sesto giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5ae-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="df5ae-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="df5ae-246"><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del settimo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="df5ae-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5ae-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="df5ae-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="df5ae-248"><strong>Windows Me/98, windows 2000:</strong> Formati anno/mese per i calendari specificati.</span><span class="sxs-lookup"><span data-stu-id="df5ae-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="df5ae-249">Se il nome nativo per il giorno della settimana o per un mese è una stringa vuota, tale nome è identico al nome specificato nelle informazioni sulle impostazioni locali corrispondenti e pertanto non viene duplicato qui.</span><span class="sxs-lookup"><span data-stu-id="df5ae-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




