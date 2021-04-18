---
description: S2359 delle impostazioni locali \_ e \_ SPM locale
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 e LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315483"
---
# <a name="locale_s2359-and-locale_spm"></a><span data-ttu-id="deaf8-103">S2359 delle impostazioni locali \_ e \_ SPM locale</span><span class="sxs-lookup"><span data-stu-id="deaf8-103">LOCALE\_S2359 and LOCALE\_SPM</span></span>

<span data-ttu-id="deaf8-104">Stringa per l'indicatore PM (seconda 12 ore del giorno).</span><span class="sxs-lookup"><span data-stu-id="deaf8-104">String for the PM designator (second 12 hours of the day).</span></span> <span data-ttu-id="deaf8-105">Il numero massimo di caratteri consentiti per questa stringa è diverso per le diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="deaf8-105">The maximum number of characters allowed for this string is different for different releases of Windows.</span></span>

<span data-ttu-id="deaf8-106">**Windows XP:** Tredici, incluso un carattere null di terminazione per [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="deaf8-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="deaf8-107">Quindici, incluso un carattere null di terminazione per [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="deaf8-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="deaf8-108">**Windows Me/98/95, Windows NT 4,0, windows 2000:** Nine che include un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="deaf8-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="deaf8-109">**Windows Server 2003 e versioni successive:** Quindici, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="deaf8-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="deaf8-110">Windows 10 ha aggiunto il valore delle **impostazioni locali \_ SPM** come sinonimo più leggibile per le **impostazioni locali \_ S2359**.</span><span class="sxs-lookup"><span data-stu-id="deaf8-110">Windows 10 added the value **LOCALE\_SPM** as a more readable synonym for **LOCALE\_S2359**.</span></span>

 

 



