---
description: Questo argomento definisce gli identificatori di calendario (tipo di dati CALId) usati per specificare calendari diversi.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificatori del calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751154"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="83fa1-103">Identificatori del calendario</span><span class="sxs-lookup"><span data-stu-id="83fa1-103">Calendar Identifiers</span></span>

<span data-ttu-id="83fa1-104">Questo argomento definisce gli identificatori di calendario (tipo di dati CALId) usati per specificare calendari diversi.</span><span class="sxs-lookup"><span data-stu-id="83fa1-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="83fa1-105">Le applicazioni possono usare questi identificatori quando usano le funzioni NLS e le funzioni di callback seguenti, che hanno parametri che accettano il tipo di dati CALId:</span><span class="sxs-lookup"><span data-stu-id="83fa1-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="83fa1-106">**ConvertSystemTimeToCalDateTime**</span><span class="sxs-lookup"><span data-stu-id="83fa1-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="83fa1-107">**EnumCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="83fa1-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="83fa1-108">**EnumCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="83fa1-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="83fa1-109">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="83fa1-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="83fa1-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83fa1-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="83fa1-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83fa1-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="83fa1-112">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="83fa1-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="83fa1-113">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="83fa1-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="83fa1-114">**GetCalendarSupportedDateRange**</span><span class="sxs-lookup"><span data-stu-id="83fa1-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="83fa1-115">**IsCalendarLeapYear**</span><span class="sxs-lookup"><span data-stu-id="83fa1-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="83fa1-116">**SetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="83fa1-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="83fa1-117">Vengono definiti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="83fa1-117">The following values are defined.</span></span> <span data-ttu-id="83fa1-118">Tutti gli altri valori sono riservati.</span><span class="sxs-lookup"><span data-stu-id="83fa1-118">All other values are reserved.</span></span> <span data-ttu-id="83fa1-119">Questi valori non possono essere combinati tra loro.</span><span class="sxs-lookup"><span data-stu-id="83fa1-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="83fa1-120">Identificatore calendario</span><span class="sxs-lookup"><span data-stu-id="83fa1-120">Calendar identifier</span></span>

<span data-ttu-id="83fa1-121">Significato</span><span class="sxs-lookup"><span data-stu-id="83fa1-121">Meaning</span></span>

<span data-ttu-id="83fa1-122">1</span><span class="sxs-lookup"><span data-stu-id="83fa1-122">1</span></span>

<span data-ttu-id="83fa1-123">\_gregoriano Cal</span><span class="sxs-lookup"><span data-stu-id="83fa1-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="83fa1-124">Gregoriano (localizzato)</span><span class="sxs-lookup"><span data-stu-id="83fa1-124">Gregorian (localized)</span></span>

<span data-ttu-id="83fa1-125">2</span><span class="sxs-lookup"><span data-stu-id="83fa1-125">2</span></span>

<span data-ttu-id="83fa1-126">CAL \_ Gregorian \_ US</span><span class="sxs-lookup"><span data-stu-id="83fa1-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="83fa1-127">Gregoriano (stringhe inglesi sempre)</span><span class="sxs-lookup"><span data-stu-id="83fa1-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="83fa1-128">3</span><span class="sxs-lookup"><span data-stu-id="83fa1-128">3</span></span>

<span data-ttu-id="83fa1-129">CAL \_ Giappone</span><span class="sxs-lookup"><span data-stu-id="83fa1-129">CAL\_JAPAN</span></span>

<span data-ttu-id="83fa1-130">Era giapponese imperatore</span><span class="sxs-lookup"><span data-stu-id="83fa1-130">Japanese Emperor Era</span></span>

<span data-ttu-id="83fa1-131">4</span><span class="sxs-lookup"><span data-stu-id="83fa1-131">4</span></span>

<span data-ttu-id="83fa1-132">CAL \_ Taiwan</span><span class="sxs-lookup"><span data-stu-id="83fa1-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="83fa1-133">Calendario di Taiwan</span><span class="sxs-lookup"><span data-stu-id="83fa1-133">Taiwan calendar</span></span>

<span data-ttu-id="83fa1-134">5</span><span class="sxs-lookup"><span data-stu-id="83fa1-134">5</span></span>

<span data-ttu-id="83fa1-135">CAL \_ Corea</span><span class="sxs-lookup"><span data-stu-id="83fa1-135">CAL\_KOREA</span></span>

<span data-ttu-id="83fa1-136">Era Tangun coreano</span><span class="sxs-lookup"><span data-stu-id="83fa1-136">Korean Tangun Era</span></span>

<span data-ttu-id="83fa1-137">6</span><span class="sxs-lookup"><span data-stu-id="83fa1-137">6</span></span>

<span data-ttu-id="83fa1-138">\_Hijri Cal</span><span class="sxs-lookup"><span data-stu-id="83fa1-138">CAL\_HIJRI</span></span>

<span data-ttu-id="83fa1-139">Hijri (arabo lunare)</span><span class="sxs-lookup"><span data-stu-id="83fa1-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="83fa1-140">7</span><span class="sxs-lookup"><span data-stu-id="83fa1-140">7</span></span>

<span data-ttu-id="83fa1-141">CAL \_ Thai</span><span class="sxs-lookup"><span data-stu-id="83fa1-141">CAL\_THAI</span></span>

<span data-ttu-id="83fa1-142">Thai</span><span class="sxs-lookup"><span data-stu-id="83fa1-142">Thai</span></span>

<span data-ttu-id="83fa1-143">8</span><span class="sxs-lookup"><span data-stu-id="83fa1-143">8</span></span>

<span data-ttu-id="83fa1-144">\_inglese Cal</span><span class="sxs-lookup"><span data-stu-id="83fa1-144">CAL\_HEBREW</span></span>

<span data-ttu-id="83fa1-145">Ebraico (lunare)</span><span class="sxs-lookup"><span data-stu-id="83fa1-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="83fa1-146">9</span><span class="sxs-lookup"><span data-stu-id="83fa1-146">9</span></span>

<span data-ttu-id="83fa1-147">CAL \_ gregoriano \_ \_ francese</span><span class="sxs-lookup"><span data-stu-id="83fa1-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="83fa1-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="83fa1-148">Gregorian Middle East French</span></span>

<span data-ttu-id="83fa1-149">10</span><span class="sxs-lookup"><span data-stu-id="83fa1-149">10</span></span>

<span data-ttu-id="83fa1-150">CAL \_ gregoriano \_ arabo</span><span class="sxs-lookup"><span data-stu-id="83fa1-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="83fa1-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="83fa1-151">Gregorian Arabic</span></span>

<span data-ttu-id="83fa1-152">11</span><span class="sxs-lookup"><span data-stu-id="83fa1-152">11</span></span>

<span data-ttu-id="83fa1-153">CAL \_ gregoriano \_ XLIT \_ inglese</span><span class="sxs-lookup"><span data-stu-id="83fa1-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="83fa1-154">Lingua inglese (gregoriano) traslitterato</span><span class="sxs-lookup"><span data-stu-id="83fa1-154">Gregorian transliterated English</span></span>

<span data-ttu-id="83fa1-155">12</span><span class="sxs-lookup"><span data-stu-id="83fa1-155">12</span></span>

<span data-ttu-id="83fa1-156">CAL \_ gregoriano \_ XLIT \_ francese</span><span class="sxs-lookup"><span data-stu-id="83fa1-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="83fa1-157">Gregoriano traslitterato francese</span><span class="sxs-lookup"><span data-stu-id="83fa1-157">Gregorian transliterated French</span></span>

<span data-ttu-id="83fa1-158">23</span><span class="sxs-lookup"><span data-stu-id="83fa1-158">23</span></span>

<span data-ttu-id="83fa1-159">\_UMALQURA Cal</span><span class="sxs-lookup"><span data-stu-id="83fa1-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="83fa1-160">**Windows Vista e versioni successive:** Calendario Um al Qura (arabo lunare)</span><span class="sxs-lookup"><span data-stu-id="83fa1-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="83fa1-161">Il gap di numerazione tra gli identificatori CAL \_ gregoriano \_ XLIT \_ francese e Cal \_ UMALQURA è intenzionale.</span><span class="sxs-lookup"><span data-stu-id="83fa1-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="83fa1-162">L'indicatore per CAL \_ UMALQURA è 23, non 13.</span><span class="sxs-lookup"><span data-stu-id="83fa1-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="83fa1-163">Inoltre, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) e [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) consentono l'uso del valore enum \_ All \_ Calendars per richiedere un'enumerazione di tutti i calendari applicabili.</span><span class="sxs-lookup"><span data-stu-id="83fa1-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="83fa1-164">Valore</span><span class="sxs-lookup"><span data-stu-id="83fa1-164">Value</span></span>

<span data-ttu-id="83fa1-165">Significato</span><span class="sxs-lookup"><span data-stu-id="83fa1-165">Meaning</span></span>

<span data-ttu-id="83fa1-166">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="83fa1-166">0xffffffff</span></span>

<span data-ttu-id="83fa1-167">ENUMERA \_ tutti i \_ calendari</span><span class="sxs-lookup"><span data-stu-id="83fa1-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="83fa1-168">Tutti i calendari applicabili per le impostazioni locali specificate</span><span class="sxs-lookup"><span data-stu-id="83fa1-168">All applicable calendars for the specified locale</span></span>



 

 

 
