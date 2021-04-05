---
description: A ogni impostazioni locali è associato un tipo di calendario predefinito (tipo di dati CALTYPE). Le impostazioni locali possono anche avere un tipo di calendario alternativo. Per informazioni dettagliate sui tipi di calendario, vedere informazioni sul tipo di calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Data e calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884581"
---
# <a name="date-and-calendar"></a><span data-ttu-id="061bc-105">Data e calendario</span><span class="sxs-lookup"><span data-stu-id="061bc-105">Date and Calendar</span></span>

<span data-ttu-id="061bc-106">A ogni [impostazioni locali](locales-and-languages.md) è associato un tipo di calendario predefinito (tipo di dati CALTYPE).</span><span class="sxs-lookup"><span data-stu-id="061bc-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="061bc-107">Le impostazioni locali possono anche avere un tipo di calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="061bc-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="061bc-108">Per informazioni dettagliate sui tipi di calendario, vedere [informazioni sul tipo di calendario](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="061bc-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="061bc-109">Per usare un tipo di calendario alternativo per le impostazioni locali, l'applicazione deve impostare la costante [ \_ IOPTIONALCALENDAR delle impostazioni locali](locale-ioptionalcalendar.md) sul tipo di calendario alternativo per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="061bc-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="061bc-110">La maggior parte delle impostazioni locali utilizza il calendario gregoriano standard e un numero impostato di formati di data.</span><span class="sxs-lookup"><span data-stu-id="061bc-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="061bc-111">Queste opzioni predefinite per i formati di data sono disponibili per la visualizzazione tramite la funzione [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .</span><span class="sxs-lookup"><span data-stu-id="061bc-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="061bc-112">Alcune impostazioni locali richiedono considerazioni speciali quando si crea un elenco completo di opzioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="061bc-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="061bc-113">Per alcune di queste impostazioni locali è necessario inserire stringhe di testo nella stringa di formato della data, mentre altre richiedono un metodo di calcolo dei valori completamente diverso.</span><span class="sxs-lookup"><span data-stu-id="061bc-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="061bc-114">Un'applicazione soddisfa questi requisiti speciali mediante l'aggiunta di determinati tipi di informazioni sulle impostazioni locali e tipi di calendario.</span><span class="sxs-lookup"><span data-stu-id="061bc-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="061bc-115">Per informazioni dettagliate sull'implementazione di date e calendari nelle applicazioni, vedere [recupero di informazioni su data e ora](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="061bc-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="061bc-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="061bc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="061bc-117">Informazioni sul supporto linguistico nazionale</span><span class="sxs-lookup"><span data-stu-id="061bc-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="061bc-118">Informazioni sul tipo di calendario</span><span class="sxs-lookup"><span data-stu-id="061bc-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="061bc-119">Recupero di informazioni su data e ora</span><span class="sxs-lookup"><span data-stu-id="061bc-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="061bc-120">**EnumDateFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="061bc-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="061bc-121">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="061bc-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



