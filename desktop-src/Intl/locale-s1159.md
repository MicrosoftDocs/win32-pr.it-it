---
description: Impostazioni locali \_ S1159 e Sam locale \_
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 e LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883697"
---
# <a name="locale_s1159-and-locale_sam"></a><span data-ttu-id="7b7db-103">Impostazioni locali \_ S1159 e Sam locale \_</span><span class="sxs-lookup"><span data-stu-id="7b7db-103">LOCALE\_S1159 and LOCALE\_SAM</span></span>

<span data-ttu-id="7b7db-104">Stringa per l'indicatore AM (prime 12 ore del giorno).</span><span class="sxs-lookup"><span data-stu-id="7b7db-104">String for the AM designator (first 12 hours of the day).</span></span> <span data-ttu-id="7b7db-105">Il numero massimo di caratteri consentiti per questa stringa, incluso un carattere di terminazione null, è diverso per le diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b7db-105">The maximum number of characters allowed for this string, including a terminating null character, is different for different releases of Windows.</span></span>

<span data-ttu-id="7b7db-106">**Windows XP:** Tredici, incluso un carattere null di terminazione per [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="7b7db-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="7b7db-107">Quindici, incluso un carattere null di terminazione per [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="7b7db-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="7b7db-108">**Windows Me/98/95, Windows NT 4,0, windows 2000:** Nine che include un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="7b7db-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="7b7db-109">**Windows Server 2003 e versioni successive:** Quindici, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="7b7db-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="7b7db-110">Windows 10 ha aggiunto il valore **locale \_ Sam** come sinonimo più leggibile per le **impostazioni locali \_ S1159**.</span><span class="sxs-lookup"><span data-stu-id="7b7db-110">Windows 10 added the value **LOCALE\_SAM** as a more readable synonym for **LOCALE\_S1159**.</span></span>

 

 



