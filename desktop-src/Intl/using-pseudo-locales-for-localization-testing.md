---
description: In Windows Vista e versioni successive, è possibile utilizzare pseudo-impostazioni locali per testare la localizzabilità delle applicazioni. In questo argomento sono incluse le procedure per l'utilizzo di pseudo-codici.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Utilizzo di pseudo-impostazioni locali per i test di localizzabilità
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319473"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="bd3cd-104">Utilizzo di pseudo-impostazioni locali per i test di localizzabilità</span><span class="sxs-lookup"><span data-stu-id="bd3cd-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="bd3cd-105">Le [pseudo-impostazioni locali](pseudo-locales.md) sono incorporate in Windows Vista e versioni successive, in modo che sia possibile accedervi tramite le API NLS (National Language Support).</span><span class="sxs-lookup"><span data-stu-id="bd3cd-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="bd3cd-106">È possibile utilizzare le pseudo-impostazioni locali per testare la [localizzabilità](/windows/uwp/design/globalizing/globalizing-portal) delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="bd3cd-107">In questo argomento sono incluse le procedure per l'utilizzo di pseudo-codici.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="bd3cd-108">Un'attività che richiede particolare attenzione quando si tratta di pseudo-impostazioni locali li enumera; sia nel codice che nella parte relativa alle opzioni internazionali e della lingua del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="bd3cd-109">Ulteriori informazioni su più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-109">More on that later in this topic.</span></span>

<span data-ttu-id="bd3cd-110">I nomi delle pseudo-impostazioni locali sono "query al secondo-ploc", "query al secondo-Besca" e "query al secondo-plocm".</span><span class="sxs-lookup"><span data-stu-id="bd3cd-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="bd3cd-111">A partire da Windows 10, sono disponibili anche le pseudo-impostazioni locali "query al secondo-Latn-x-SH".</span><span class="sxs-lookup"><span data-stu-id="bd3cd-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="bd3cd-112">Recuperare informazioni sulle pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="bd3cd-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="bd3cd-113">È possibile usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) per recuperare informazioni su pseudo-impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="bd3cd-114">Passare alla funzione il nome delle pseudo-impostazioni locali specifiche. vedere l'elenco dei nomi precedenti.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="bd3cd-115">Ad esempio, "query al secondo-plocm" per le pseudo-impostazioni locali con mirroring.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="bd3cd-116">Usare LocaleNameToLCID con pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="bd3cd-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="bd3cd-117">È possibile chiamare la funzione di mapping NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con il nome di una pseudo-impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="bd3cd-118">Abilita pseudo-impostazioni locali per l'enumerazione</span><span class="sxs-lookup"><span data-stu-id="bd3cd-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="bd3cd-119">Nell'applicazione è possibile chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) per enumerare le impostazioni locali riconosciute dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="bd3cd-120">La parte opzioni internazionali e della lingua del pannello di controllo chiama anche **EnumSystemLocalesEx** per compilare l'elenco delle impostazioni locali che Visualizza.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="bd3cd-121">Tuttavia, per impostazione predefinita, le quattro pseudo-impostazioni locali elencate in precedenza non vengono riconosciute dal sistema, pertanto non verranno restituite da **EnumSystemLocalesEx**.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="bd3cd-122">Per i sistemi di Windows Vista fino a Windows 10, versione 1709, la soluzione consiste nell'abilitare le pseudo-impostazioni locali aggiungendo chiavi al registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="bd3cd-123">Le modifiche vengono apportate sotto la \_ \_ \\ \\ chiave NLS del controllo CurrentControlSet di HKEY Local Machine System \\ \\ per le lingue installate nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="bd3cd-124">È possibile impostare queste impostazioni per abilitare le pseudo-impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="bd3cd-125">Ogni chiave mostrata di seguito è l'LCID esadecimale corrispondente alle pseudo-impostazioni locali che vengono abilitate.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="bd3cd-126">Ogni valore è di tipo stringa (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="bd3cd-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="bd3cd-127">Per Windows 10, versione 1803, la modifica del registro di sistema di Windows come questa non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="bd3cd-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="bd3cd-128">Tuttavia, è comunque possibile chiamare le API NLS non di enumerazione con i nomi delle pseudo-impostazioni locali (vedere gli esempi di codice precedenti) per popolare l'interfaccia utente (UI).</span><span class="sxs-lookup"><span data-stu-id="bd3cd-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd3cd-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd3cd-129">Related topics</span></span>

* [<span data-ttu-id="bd3cd-130">Uso del supporto per le lingue nazionali</span><span class="sxs-lookup"><span data-stu-id="bd3cd-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="bd3cd-131">Pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="bd3cd-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="bd3cd-132">EnumSystemLocalesEx</span><span class="sxs-lookup"><span data-stu-id="bd3cd-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="bd3cd-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="bd3cd-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="bd3cd-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="bd3cd-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
