---
description: Il termine &\# 0034; language&\# 0034; indica una raccolta di proprietà utilizzate per la comunicazione pronunciata e scritta.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Impostazioni locali e lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308706"
---
# <a name="locales-and-languages"></a><span data-ttu-id="41a2b-103">Impostazioni locali e lingue</span><span class="sxs-lookup"><span data-stu-id="41a2b-103">Locales and Languages</span></span>

<span data-ttu-id="41a2b-104">Il termine "lingua" indica una raccolta di proprietà utilizzate per la comunicazione vocale e scritta.</span><span class="sxs-lookup"><span data-stu-id="41a2b-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="41a2b-105">Ogni lingua dispone di un nome di lingua e di un identificatore di lingua che indicano la [tabella codici](code-pages.md) specifica (ANSI, DOS, Macintosh) utilizzata per rappresentare la [posizione geografica](table-of-geographical-locations.md) per la lingua del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="41a2b-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="41a2b-106">Una lingua neutra è indicata da un nome, ad esempio "en" per l'inglese.</span><span class="sxs-lookup"><span data-stu-id="41a2b-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="41a2b-107">Un linguaggio più geograficamente specifico può essere indicato da un nome che include le informazioni sulle impostazioni locali e il paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="41a2b-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="41a2b-108">Ad esempio, le impostazioni locali Inglese (Stati Uniti) hanno il nome della lingua "en-US".</span><span class="sxs-lookup"><span data-stu-id="41a2b-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="41a2b-109">Le "impostazioni locali" sono una raccolta di informazioni sulle preferenze utente correlate al linguaggio rappresentate come un elenco di valori.</span><span class="sxs-lookup"><span data-stu-id="41a2b-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="41a2b-110">Windows XP supporta più di 150 impostazioni locali e Windows Vista supporta circa 200.</span><span class="sxs-lookup"><span data-stu-id="41a2b-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="41a2b-111">Ogni impostazione locale è definita da un linguaggio e un ordinamento e ha sia un nome delle impostazioni locali che un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="41a2b-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="41a2b-112">Un esempio di nome delle impostazioni locali per la lingua tedesca (Germania) è "de-DE \_ Rubrica".</span><span class="sxs-lookup"><span data-stu-id="41a2b-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="41a2b-113">Ogni sistema operativo ha almeno un'impostazione locale installata e spesso ha molte impostazioni locali da cui l'utente può selezionare.</span><span class="sxs-lookup"><span data-stu-id="41a2b-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="41a2b-114">A ogni impostazione locale sono associate numerose informazioni, tranne il nome e l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="41a2b-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="41a2b-115">I tipi di informazioni sulle impostazioni locali sono descritti in [costanti di informazioni sulle impostazioni locali](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="41a2b-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="41a2b-116">Il sistema operativo assegna impostazioni locali a ogni thread, assegnando inizialmente le impostazioni locali predefinite del sistema, definite dalle [impostazioni locali del \_ sistema \_ ](locale-system-default.md).</span><span class="sxs-lookup"><span data-stu-id="41a2b-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="41a2b-117">Le impostazioni locali vengono impostate quando viene installato il sistema operativo o quando l'utente lo seleziona utilizzando la parte opzioni internazionali e della lingua del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="41a2b-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="41a2b-118">Quando si esegue un thread in un processo appartenente all'utente, il sistema operativo assegna al thread le impostazioni locali predefinite dell'utente.</span><span class="sxs-lookup"><span data-stu-id="41a2b-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="41a2b-119">Questa impostazione locale è definita da [impostazioni locali \_ dell' \_ utente](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="41a2b-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="41a2b-120">Un'applicazione può eseguire l'override di entrambi i valori predefiniti utilizzando la funzione [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) per impostare in modo esplicito le impostazioni locali per un thread.</span><span class="sxs-lookup"><span data-stu-id="41a2b-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="41a2b-121">Per l'implementazione di un linguaggio è necessario specificare le impostazioni locali corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="41a2b-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="41a2b-122">Il sistema operativo implementa una lingua neutra selezionando i dati per le impostazioni locali associate a una versione specifica del linguaggio, in genere le impostazioni locali più diffuse.</span><span class="sxs-lookup"><span data-stu-id="41a2b-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="41a2b-123">A partire da Windows Vista, è possibile che una determinata lingua corrisponda a un'impostazione locale supplementare, ovvero un tipo di impostazioni locali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="41a2b-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="41a2b-124">Poiché tutte le impostazioni locali aggiuntive condividono un solo identificatore delle impostazioni locali, le applicazioni devono gestire queste impostazioni locali e le lingue corrispondenti per nome anziché per identificatore.</span><span class="sxs-lookup"><span data-stu-id="41a2b-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="41a2b-125">I concetti relativi alla lingua sono strettamente correlati ai concetti locali, ma i due termini non sono intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="41a2b-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="41a2b-126">Come regola generale, le funzioni correlate all' [interfaccia utente multilingue](multilingual-user-interface.md) gestiscono le lingue, mentre le funzioni NLS agiscono sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="41a2b-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="41a2b-127">Questo articolo descrive gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="41a2b-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="41a2b-128">Impostazioni locali personalizzate</span><span class="sxs-lookup"><span data-stu-id="41a2b-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="41a2b-129">Identificatori di lingua</span><span class="sxs-lookup"><span data-stu-id="41a2b-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="41a2b-130">Nomi di lingua</span><span class="sxs-lookup"><span data-stu-id="41a2b-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="41a2b-131">Identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="41a2b-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="41a2b-132">Nomi delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="41a2b-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="41a2b-133">Pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="41a2b-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="41a2b-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41a2b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a2b-135">Informazioni sul supporto linguistico nazionale</span><span class="sxs-lookup"><span data-stu-id="41a2b-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="41a2b-136">Tabelle codici</span><span class="sxs-lookup"><span data-stu-id="41a2b-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="41a2b-137">Costanti di informazioni sulle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="41a2b-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="41a2b-138">Interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="41a2b-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="41a2b-139">Tabella delle posizioni geografiche</span><span class="sxs-lookup"><span data-stu-id="41a2b-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="41a2b-140">Gestione della lingua dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="41a2b-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="41a2b-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="41a2b-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



