---
description: impostazioni locali \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307850"
---
# <a name="locale_sscripts"></a><span data-ttu-id="19605-103">impostazioni locali \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="19605-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="19605-104">**Windows Vista e versioni successive:** Stringa che rappresenta un elenco di script, utilizzando la notazione di 4 caratteri utilizzata in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="19605-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="19605-105">Ogni nome di script è costituito da quattro caratteri latini e l'elenco viene disposto in ordine alfabetico con ogni nome, incluso l'ultimo, seguito da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="19605-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="19605-106">È possibile chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su locale \_ SSCRIPTS come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi di dominio internazionali (IDN).</span><span class="sxs-lookup"><span data-stu-id="19605-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="19605-107">Di seguito sono riportati alcuni valori di esempio:</span><span class="sxs-lookup"><span data-stu-id="19605-107">Here are some example values:</span></span>



| <span data-ttu-id="19605-108">Locale</span><span class="sxs-lookup"><span data-stu-id="19605-108">Locale</span></span>                  | <span data-ttu-id="19605-109">Nome delle impostazioni locali/lingua</span><span class="sxs-lookup"><span data-stu-id="19605-109">Locale/language name</span></span> | <span data-ttu-id="19605-110">Valore</span><span class="sxs-lookup"><span data-stu-id="19605-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19605-111">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="19605-111">English (United States)</span></span> | <span data-ttu-id="19605-112">it-IT</span><span class="sxs-lookup"><span data-stu-id="19605-112">en-US</span></span>                | <span data-ttu-id="19605-113">Latn</span><span class="sxs-lookup"><span data-stu-id="19605-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="19605-114">Hindi (India)</span><span class="sxs-lookup"><span data-stu-id="19605-114">Hindi (India)</span></span>           | <span data-ttu-id="19605-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="19605-115">hi-IN</span></span>                | <span data-ttu-id="19605-116">Deva</span><span class="sxs-lookup"><span data-stu-id="19605-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="19605-117">Giapponese (Giappone)</span><span class="sxs-lookup"><span data-stu-id="19605-117">Japanese (Japan)</span></span>        | <span data-ttu-id="19605-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="19605-118">ja-JP</span></span>                | <span data-ttu-id="19605-119">**Windows 7 e versioni successive:** Hani Hira Jpan; Kana</span><span class="sxs-lookup"><span data-stu-id="19605-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="19605-120">**Windows Vista:** Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="19605-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="19605-121">Un valore di script composto non include lo script latino, a meno che non si tratti di una parte essenziale del sistema di scrittura usato per le impostazioni locali specifiche.</span><span class="sxs-lookup"><span data-stu-id="19605-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="19605-122">I caratteri latini vengono spesso utilizzati nel contesto delle impostazioni locali per le quali non sono nativi, ad esempio per un nome aziendale esterno.</span><span class="sxs-lookup"><span data-stu-id="19605-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="19605-123">Nell'esempio precedente per hindi in India, l'unico valore di script è "Deva" (per "devangal"), anche se i caratteri latini possono essere visualizzati anche in testo Hindi.</span><span class="sxs-lookup"><span data-stu-id="19605-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="19605-124">La funzione [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) ha un flag speciale per risolvere questo caso.</span><span class="sxs-lookup"><span data-stu-id="19605-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




