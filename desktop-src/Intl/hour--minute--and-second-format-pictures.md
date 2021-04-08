---
description: Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale. Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Immagini di formato ora, minuto e secondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058360"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="4d126-104">Immagini di formato ora, minuto e secondo</span><span class="sxs-lookup"><span data-stu-id="4d126-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="4d126-105">Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale.</span><span class="sxs-lookup"><span data-stu-id="4d126-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="4d126-106">Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="4d126-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="4d126-107">Nei tipi di formato le lettere "m", "s" e "t" devono essere minuscole e la lettera "h" deve essere minuscola per indicare il formato a 12 ore o maiuscolo ("H") per indicare il formato a 24 ore.</span><span class="sxs-lookup"><span data-stu-id="4d126-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="4d126-108">È possibile utilizzare le virgolette singole per contrassegnare i caratteri che devono essere visualizzati esattamente come specificato.</span><span class="sxs-lookup"><span data-stu-id="4d126-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="4d126-109">Se l'applicazione deve visualizzare una virgoletta singola, deve inserire due virgolette singole in una riga.</span><span class="sxs-lookup"><span data-stu-id="4d126-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="4d126-110">Ad esempio,' ABC '' barra ' viene visualizzato come "abc'bar".</span><span class="sxs-lookup"><span data-stu-id="4d126-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="4d126-111">Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare le ore.</span><span class="sxs-lookup"><span data-stu-id="4d126-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="4d126-112">string</span><span class="sxs-lookup"><span data-stu-id="4d126-112">String</span></span> | <span data-ttu-id="4d126-113">Significato</span><span class="sxs-lookup"><span data-stu-id="4d126-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="4d126-114">h</span><span class="sxs-lookup"><span data-stu-id="4d126-114">h</span></span>      | <span data-ttu-id="4d126-115">Ore senza zeri iniziali per le ore a una sola cifra (orario a 12 ore).</span><span class="sxs-lookup"><span data-stu-id="4d126-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="4d126-116">hh</span><span class="sxs-lookup"><span data-stu-id="4d126-116">hh</span></span>     | <span data-ttu-id="4d126-117">Ore con zeri iniziali per le ore a una sola cifra (orario a 12 ore).</span><span class="sxs-lookup"><span data-stu-id="4d126-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="4d126-118">H</span><span class="sxs-lookup"><span data-stu-id="4d126-118">H</span></span>      | <span data-ttu-id="4d126-119">Ore senza zeri iniziali per le ore a una sola cifra (orario a 24 ore).</span><span class="sxs-lookup"><span data-stu-id="4d126-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="4d126-120">HH</span><span class="sxs-lookup"><span data-stu-id="4d126-120">HH</span></span>     | <span data-ttu-id="4d126-121">Ore con zeri iniziali per le ore a una sola cifra (orario a 24 ore).</span><span class="sxs-lookup"><span data-stu-id="4d126-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="4d126-122">Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i minuti.</span><span class="sxs-lookup"><span data-stu-id="4d126-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="4d126-123">string</span><span class="sxs-lookup"><span data-stu-id="4d126-123">String</span></span> | <span data-ttu-id="4d126-124">Significato</span><span class="sxs-lookup"><span data-stu-id="4d126-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="4d126-125">m</span><span class="sxs-lookup"><span data-stu-id="4d126-125">m</span></span>      | <span data-ttu-id="4d126-126">Minuti senza zeri iniziali per minuti a una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="4d126-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="4d126-127">MM</span><span class="sxs-lookup"><span data-stu-id="4d126-127">mm</span></span>     | <span data-ttu-id="4d126-128">Minuti con zeri iniziali per minuti a una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="4d126-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="4d126-129">Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i secondi.</span><span class="sxs-lookup"><span data-stu-id="4d126-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="4d126-130">string</span><span class="sxs-lookup"><span data-stu-id="4d126-130">String</span></span> | <span data-ttu-id="4d126-131">Significato</span><span class="sxs-lookup"><span data-stu-id="4d126-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="4d126-132">s</span><span class="sxs-lookup"><span data-stu-id="4d126-132">s</span></span>      | <span data-ttu-id="4d126-133">Secondi senza zeri iniziali per i secondi a una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="4d126-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="4d126-134">ss</span><span class="sxs-lookup"><span data-stu-id="4d126-134">ss</span></span>     | <span data-ttu-id="4d126-135">Secondi con zeri iniziali per i secondi a una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="4d126-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="4d126-136">Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare un marcatore temporale.</span><span class="sxs-lookup"><span data-stu-id="4d126-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="4d126-137">string</span><span class="sxs-lookup"><span data-stu-id="4d126-137">String</span></span> | <span data-ttu-id="4d126-138">Significato</span><span class="sxs-lookup"><span data-stu-id="4d126-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="4d126-139">u</span><span class="sxs-lookup"><span data-stu-id="4d126-139">t</span></span>      | <span data-ttu-id="4d126-140">Stringa del marcatore del tempo di un solo carattere.</span><span class="sxs-lookup"><span data-stu-id="4d126-140">One-character time marker string.</span></span><br /><span data-ttu-id="4d126-141">**Nota:** Questo formato non è consigliato per l'uso con determinate lingue, ad esempio giapponese (Giappone).</span><span class="sxs-lookup"><span data-stu-id="4d126-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="4d126-142">Con questo formato, un'applicazione accetta sempre il primo carattere dalla stringa del marcatore temporale, definito da [LOCALE_S1159](locale-s1159.md) (AM) e [LOCALE_S2359](locale-s2359.md) (PM).</span><span class="sxs-lookup"><span data-stu-id="4d126-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="4d126-143">Per questo motivo, l'applicazione può creare una formattazione non corretta con la stessa stringa utilizzata sia per AM che per PM.</span><span class="sxs-lookup"><span data-stu-id="4d126-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="4d126-144">tt</span><span class="sxs-lookup"><span data-stu-id="4d126-144">tt</span></span>     | <span data-ttu-id="4d126-145">Stringa del marcatore del tempo multicarattere.</span><span class="sxs-lookup"><span data-stu-id="4d126-145">Multi-character time marker string.</span></span> |
