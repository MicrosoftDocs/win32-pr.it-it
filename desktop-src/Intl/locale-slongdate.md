---
description: impostazioni locali \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129686"
---
# <a name="locale_slongdate"></a><span data-ttu-id="a93fb-103">impostazioni locali \_ SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="a93fb-103">LOCALE\_SLONGDATE</span></span>

<span data-ttu-id="a93fb-104">Stringa di formattazione della data estesa per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="a93fb-104">Long date formatting string for the locale.</span></span> <span data-ttu-id="a93fb-105">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a93fb-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="a93fb-106">La stringa può essere costituita da una combinazione di [Immagini di formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md) e qualsiasi stringa di caratteri racchiusa tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="a93fb-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md) and any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="a93fb-107">I caratteri racchiusi tra virgolette singole rimangono come specificato.</span><span class="sxs-lookup"><span data-stu-id="a93fb-107">Characters in single quotes remain as specified.</span></span> <span data-ttu-id="a93fb-108">Ad esempio, la data estesa spagnola (Spagna) è "dddd, DD" de "MMMM" de "aaaa".</span><span class="sxs-lookup"><span data-stu-id="a93fb-108">For example, the Spanish (Spain) long date is "dddd, dd' de 'MMMM' de 'yyyy".</span></span> <span data-ttu-id="a93fb-109">Le impostazioni locali possono definire più formati di data estesa.</span><span class="sxs-lookup"><span data-stu-id="a93fb-109">Locales can define multiple long date formats.</span></span>

<span data-ttu-id="a93fb-110">Per ottenere tutti i formati di data estesa per le impostazioni locali, usare [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="a93fb-110">To get all of the long date formats for a locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



