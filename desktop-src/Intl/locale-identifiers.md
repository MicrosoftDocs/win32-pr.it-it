---
description: Ogni impostazioni locali dispone di un identificatore univoco, un valore a 32 bit costituito da un identificatore di lingua e un identificatore di ordinamento.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificatori delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305638"
---
# <a name="locale-identifiers"></a><span data-ttu-id="aeeed-103">Identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="aeeed-103">Locale Identifiers</span></span>

<span data-ttu-id="aeeed-104">Ogni [impostazioni locali](locales-and-languages.md) dispone di un identificatore univoco, un valore a 32 bit costituito da un identificatore di [lingua](language-identifiers.md) e un [identificatore di ordinamento](sort-order-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="aeeed-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="aeeed-105">L'identificatore delle impostazioni locali è un'abbreviazione numerica internazionale standard e include i componenti necessari per identificare in modo univoco una delle impostazioni locali definite dal sistema operativo installate.</span><span class="sxs-lookup"><span data-stu-id="aeeed-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="aeeed-106">NLS supporta sia gli identificatori delle impostazioni locali predefiniti sia gli identificatori personalizzati.</span><span class="sxs-lookup"><span data-stu-id="aeeed-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="aeeed-107">I nomi delle impostazioni locali possono essere utilizzati con le funzioni introdotte in Windows Vista che accettano un [nome delle impostazioni locali](locale-names.md) come parametro, anziché un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="aeeed-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="aeeed-108">Per ulteriori informazioni, vedere [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="aeeed-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="aeeed-109">L'uso di nomi delle impostazioni locali invece degli identificatori delle impostazioni locali è sempre preferibile.</span><span class="sxs-lookup"><span data-stu-id="aeeed-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="aeeed-110">Nella figura seguente viene illustrato il formato dei bit in un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="aeeed-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="aeeed-111">Identificatori delle impostazioni locali predefiniti</span><span class="sxs-lookup"><span data-stu-id="aeeed-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="aeeed-112">Gli identificatori delle impostazioni locali predefiniti supportati da NLS sono definiti nelle informazioni di [riferimento sulle API NLS (National Language Support)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span><span class="sxs-lookup"><span data-stu-id="aeeed-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="aeeed-113">NLS Usa le seguenti costanti di informazioni sulle impostazioni locali per rappresentare gli identificatori delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="aeeed-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="aeeed-114">[Impostazioni \_ locali SLANGUAGE](locale-slanguage.md) o [impostazioni locali \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="aeeed-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="aeeed-115">impostazioni locali \_ sname</span><span class="sxs-lookup"><span data-stu-id="aeeed-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="aeeed-116">impostazioni locali \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="aeeed-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="aeeed-117">impostazioni locali \_ IDEFAULTANSICODEPAGE</span><span class="sxs-lookup"><span data-stu-id="aeeed-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="aeeed-118">Identificatori delle impostazioni locali personalizzati</span><span class="sxs-lookup"><span data-stu-id="aeeed-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="aeeed-119">**Windows Vista:** NLS supporta gli identificatori delle impostazioni locali personalizzati rappresentati dalle seguenti costanti di informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="aeeed-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="aeeed-120">impostazioni locali \_ personalizzate \_ predefinite</span><span class="sxs-lookup"><span data-stu-id="aeeed-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="aeeed-121">\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="aeeed-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="aeeed-122">impostazioni locali \_ personalizzate non \_ specificate</span><span class="sxs-lookup"><span data-stu-id="aeeed-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="aeeed-123">Creazione di impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="aeeed-123">Building a Locale</span></span>

<span data-ttu-id="aeeed-124">È possibile usare l'utilità del compilatore delle impostazioni locali fornita da NLS per compilare le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="aeeed-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="aeeed-125">Per altre informazioni, vedere [Generatore di impostazioni locali Microsoft](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="aeeed-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="aeeed-126">L'applicazione può costruire un identificatore delle impostazioni locali usando la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="aeeed-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="aeeed-127">In alternativa, è possibile usare uno degli identificatori predefiniti corrispondenti alle costanti elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="aeeed-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="aeeed-128">impostazioni locali \_ INvariabili</span><span class="sxs-lookup"><span data-stu-id="aeeed-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="aeeed-129">impostazioni locali del \_ sistema \_</span><span class="sxs-lookup"><span data-stu-id="aeeed-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="aeeed-130">\_impostazione predefinita utente impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="aeeed-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="aeeed-131">Recupero degli identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="aeeed-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="aeeed-132">Un'applicazione può recuperare gli identificatori delle impostazioni locali correnti usando le funzioni [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) e [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) .</span><span class="sxs-lookup"><span data-stu-id="aeeed-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="aeeed-133">Ogni thread può impostare e recuperare le proprie impostazioni locali con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) e [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span><span class="sxs-lookup"><span data-stu-id="aeeed-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeeed-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aeeed-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeeed-135">Impostazioni locali e lingue</span><span class="sxs-lookup"><span data-stu-id="aeeed-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="aeeed-136">Identificatori di lingua</span><span class="sxs-lookup"><span data-stu-id="aeeed-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="aeeed-137">Nomi delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="aeeed-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="aeeed-138">Identificatori di ordinamento</span><span class="sxs-lookup"><span data-stu-id="aeeed-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="aeeed-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="aeeed-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
