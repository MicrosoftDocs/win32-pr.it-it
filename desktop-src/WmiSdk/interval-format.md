---
description: Definisce gli intervalli di data e ora con un formato simile alla sintassi di data e ora suddividendo la stringa nei campi per giorni, ore, minuti, secondi e microsecondi.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato intervallo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318873"
---
# <a name="interval-format"></a><span data-ttu-id="455c3-103">Formato intervallo</span><span class="sxs-lookup"><span data-stu-id="455c3-103">Interval Format</span></span>

<span data-ttu-id="455c3-104">WMI definisce gli intervalli di data e ora con un formato simile alla sintassi di data e ora suddividendo la stringa nei campi per giorni, ore, minuti, secondi e microsecondi.</span><span class="sxs-lookup"><span data-stu-id="455c3-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="455c3-105">Nell'esempio seguente viene illustrato il formato di un intervallo di data e ora.</span><span class="sxs-lookup"><span data-stu-id="455c3-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="455c3-106">Nella tabella seguente sono elencati i campi dell'intervallo di data/ora.</span><span class="sxs-lookup"><span data-stu-id="455c3-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="455c3-107">Campo</span><span class="sxs-lookup"><span data-stu-id="455c3-107">Field</span></span>    | <span data-ttu-id="455c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="455c3-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="455c3-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="455c3-109">dddddddd</span></span> | <span data-ttu-id="455c3-110">Otto cifre che rappresentano un numero di giorni (da 00000000 a 99999999).</span><span class="sxs-lookup"><span data-stu-id="455c3-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="455c3-111">HH</span><span class="sxs-lookup"><span data-stu-id="455c3-111">HH</span></span>       | <span data-ttu-id="455c3-112">Ora del giorno a due cifre che utilizza il formato a 24 ore (da 00 a 23).</span><span class="sxs-lookup"><span data-stu-id="455c3-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="455c3-113">MM</span><span class="sxs-lookup"><span data-stu-id="455c3-113">MM</span></span>       | <span data-ttu-id="455c3-114">Minuto a due cifre nell'ora (da 00 a 59).</span><span class="sxs-lookup"><span data-stu-id="455c3-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="455c3-115">SS</span><span class="sxs-lookup"><span data-stu-id="455c3-115">SS</span></span>       | <span data-ttu-id="455c3-116">Numero di secondi di due cifre nel minuto (da 00 a 59).</span><span class="sxs-lookup"><span data-stu-id="455c3-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="455c3-117">mmmmmm</span><span class="sxs-lookup"><span data-stu-id="455c3-117">mmmmmm</span></span>   | <span data-ttu-id="455c3-118">Numero di microsecondi a sei cifre nel secondo (da 000000 a 999999).</span><span class="sxs-lookup"><span data-stu-id="455c3-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="455c3-119">L'implementazione non è necessaria per supportare la valutazione con questo campo, ma questo campo deve essere sempre presente per mantenere la natura a lunghezza fissa della stringa.</span><span class="sxs-lookup"><span data-stu-id="455c3-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="455c3-120">Gli intervalli hanno sempre una ": 000" finale come gli ultimi quattro caratteri.</span><span class="sxs-lookup"><span data-stu-id="455c3-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="455c3-121">A differenza di data e ora, inoltre, non è possibile utilizzare asterischi per indicare i campi inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="455c3-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="455c3-122">Inoltre, tutte le proprietà di tipo [CIM \_ DateTime](cim-datetime.md) che rappresentano gli intervalli devono essere contrassegnate con il qualificatore standard del [sottotipo](standard-wmi-qualifiers.md) , con il qualificatore impostato su "Interval".</span><span class="sxs-lookup"><span data-stu-id="455c3-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="455c3-123">La stringa seguente rappresenta un intervallo di 1 giorno, 12 ore, 0 minuti e 32 secondi.</span><span class="sxs-lookup"><span data-stu-id="455c3-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="455c3-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="455c3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="455c3-125">Formato di data e ora</span><span class="sxs-lookup"><span data-stu-id="455c3-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="455c3-126">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="455c3-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="455c3-127">\_DateTime CIM</span><span class="sxs-lookup"><span data-stu-id="455c3-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



