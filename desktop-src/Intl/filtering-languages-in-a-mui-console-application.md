---
description: Un'applicazione console MUI può supportare le impostazioni di sistema o le impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente. In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtraggio di lingue in un'applicazione console MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882146"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="36f21-104">Filtraggio di lingue in un'applicazione console MUI</span><span class="sxs-lookup"><span data-stu-id="36f21-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="36f21-105">Un'applicazione console MUI può supportare le impostazioni di sistema o le impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="36f21-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="36f21-106">In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="36f21-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="36f21-107">Limitare le lingue da visualizzare</span><span class="sxs-lookup"><span data-stu-id="36f21-107">Limit the Languages to Display</span></span>

<span data-ttu-id="36f21-108">A differenza di una finestra grafica, la console di Windows non è in grado di visualizzare [alfabeti complessi](uniscribe-glossary.md), ad esempio arabo, ebraico, persiano, Hindi, Urdu, Thai e molti altri.</span><span class="sxs-lookup"><span data-stu-id="36f21-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="36f21-109">Pertanto, molte lingue dell'interfaccia utente non possono essere visualizzate dalla console in qualsiasi circostanza.</span><span class="sxs-lookup"><span data-stu-id="36f21-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="36f21-110">Nella console di è possibile visualizzare solo i caratteri della singola [tabella codici OEM](code-pages.md) associata alla lingua corrente per le applicazioni non Unicode.</span><span class="sxs-lookup"><span data-stu-id="36f21-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="36f21-111">Per ogni tabella codici OEM, nella console viene utilizzato un particolare tipo di carattere e questo potrebbe non fornire una copertura completa per tale tabella codici.</span><span class="sxs-lookup"><span data-stu-id="36f21-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="36f21-112">Queste limitazioni relative alla console riducono il numero di lingue dell'interfaccia utente che possono essere visualizzate dalla console in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="36f21-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="36f21-113">Se, ad esempio, la lingua corrente per le applicazioni non Unicode è giapponese e l'utente tenta di visualizzare il testo tedesco nella console, i caratteri con dieresi non vengono visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="36f21-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="36f21-114">Se la lingua corrente per le applicazioni non Unicode è il tedesco e l'utente desidera visualizzare il testo giapponese nella console, i risultati sono molto peggiori, rendendo il testo quasi incomprensibile.</span><span class="sxs-lookup"><span data-stu-id="36f21-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="36f21-115">Quando si fornisce il supporto della console per le applicazioni MUI, tenere presente che la console fornisce solo il supporto limitato per gli [Editor del metodo di input](input-method-manager.md).</span><span class="sxs-lookup"><span data-stu-id="36f21-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="36f21-116">Impostare la lingua per l'output della console</span><span class="sxs-lookup"><span data-stu-id="36f21-116">Set the Language for Console Output</span></span>

<span data-ttu-id="36f21-117">In Windows Vista e versioni successive, un'applicazione console imposta la lingua per supportare la visualizzazione della console chiamando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="36f21-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="36f21-118">In questa chiamata, l'applicazione passa il \_ filtro della console MUI \_ nel parametro *dwFlags* e **null** per *pwszLanguagesBuffer*.</span><span class="sxs-lookup"><span data-stu-id="36f21-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="36f21-119">In alternativa, è possibile chiamare [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificatore di lingua pari a 0.</span><span class="sxs-lookup"><span data-stu-id="36f21-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="36f21-120">Questa impostazione fa in modo che la funzione selezioni la lingua che meglio supporta la visualizzazione della console.</span><span class="sxs-lookup"><span data-stu-id="36f21-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="36f21-121">In Windows XP, l'applicazione può impostare solo la lingua per l'output della console chiamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificatore di lingua pari a 0.</span><span class="sxs-lookup"><span data-stu-id="36f21-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36f21-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36f21-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36f21-123">Impostazione delle preferenze di lingua dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="36f21-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
