---
description: impostazioni locali \_ SSHORTDATE
ms.assetid: 55333a53-1205-42eb-aa1a-c248c52a8a3f
title: LOCALE_SSHORTDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15077b4466fd74c02dd53bd7324aceba9233cc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308725"
---
# <a name="locale_sshortdate"></a><span data-ttu-id="b736e-103">impostazioni locali \_ SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="b736e-103">LOCALE\_SSHORTDATE</span></span>

<span data-ttu-id="b736e-104">Stringa di formattazione della data breve per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="b736e-104">Short date formatting string for the locale.</span></span> <span data-ttu-id="b736e-105">Il numero massimo di caratteri consentiti per questa stringa è 80, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="b736e-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="b736e-106">La stringa può essere costituita da una combinazione di [Immagini di formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="b736e-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md).</span></span> <span data-ttu-id="b736e-107">Ad esempio, "M/d/aaaa" indica che il 3 settembre 2004 è scritto 9/3/2004.</span><span class="sxs-lookup"><span data-stu-id="b736e-107">For example, "M/d/yyyy" indicates that September 3, 2004 is written 9/3/2004.</span></span>

<span data-ttu-id="b736e-108">Le impostazioni locali possono definire più formati di data breve.</span><span class="sxs-lookup"><span data-stu-id="b736e-108">Locales can define multiple short date formats.</span></span> <span data-ttu-id="b736e-109">Per ottenere tutti i formati di data breve per le impostazioni locali, usare [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="b736e-109">To get all of the short date formats for this locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



