---
description: Utilizzo di dati locali persistenti
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Utilizzo di dati locali persistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885721"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="0aec5-103">Utilizzo di dati locali persistenti</span><span class="sxs-lookup"><span data-stu-id="0aec5-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="0aec5-104">Un'applicazione globalizzata spesso rende permanente o trasmette dati, ad esempio data e ora.</span><span class="sxs-lookup"><span data-stu-id="0aec5-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="0aec5-105">Quando si decide in che modo l'applicazione deve gestire la persistenza dei dati, tenere presente che i dati non sono necessariamente uguali da computer a computer o da esecuzioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0aec5-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="0aec5-106">Questo vale sia per le [impostazioni locali](locales-and-languages.md) fornite con le [impostazioni locali](custom-locales.md)di Windows che per quelle personalizzate.</span><span class="sxs-lookup"><span data-stu-id="0aec5-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="0aec5-107">La progettazione dell'applicazione deve prendere in considerazione una serie di modifiche ai dati correlate alle impostazioni locali che possono verificarsi.</span><span class="sxs-lookup"><span data-stu-id="0aec5-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="0aec5-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0aec5-108">For example:</span></span>

-   <span data-ttu-id="0aec5-109">I simboli di valuta possono cambiare quando i paesi adottano l'euro.</span><span class="sxs-lookup"><span data-stu-id="0aec5-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="0aec5-110">Le preferenze internazionali possono cambiare.</span><span class="sxs-lookup"><span data-stu-id="0aec5-110">Regional preferences can change.</span></span> <span data-ttu-id="0aec5-111">Ad esempio, il formato d/m/y potrebbe variare nel formato m/d/y per determinate impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="0aec5-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="0aec5-112">L'ortografia dei nomi dei giorni può variare a causa delle riforme ortografiche.</span><span class="sxs-lookup"><span data-stu-id="0aec5-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="0aec5-113">Inoltre, la combinazione di maiuscole e minuscole può variare per i nomi dei mesi</span><span class="sxs-lookup"><span data-stu-id="0aec5-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="0aec5-114">Usare formati di Locale-Independent per l'archiviazione e l'interscambio dati</span><span class="sxs-lookup"><span data-stu-id="0aec5-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="0aec5-115">Un'applicazione che rende permanente i dati deve usare formati indipendenti dalle impostazioni locali per l'archiviazione e l'interscambio dati.</span><span class="sxs-lookup"><span data-stu-id="0aec5-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="0aec5-116">Esempi sono formati hardcoded o standard; le impostazioni locali invariabili del [ \_ nome delle \_ Impostazioni](locale-name-constants.md)locali e dei formati di archiviazione binari.</span><span class="sxs-lookup"><span data-stu-id="0aec5-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="0aec5-117">Se sono necessari dati di ordinamento permanenti, l'applicazione deve utilizzare la funzione [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .</span><span class="sxs-lookup"><span data-stu-id="0aec5-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="0aec5-118">Tenere presente che un formato invariante non rimane invariante per l' [ordinamento](sorting.md), solo per le impostazioni locali e i dati del calendario.</span><span class="sxs-lookup"><span data-stu-id="0aec5-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="0aec5-119">Usare le impostazioni locali predefinite dell'utente per la presentazione dei dati</span><span class="sxs-lookup"><span data-stu-id="0aec5-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="0aec5-120">Per presentare i dati persistenti, è preferibile che l'applicazione riformatta i dati utilizzando le impostazioni locali predefinite dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0aec5-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="0aec5-121">L'utilizzo di queste impostazioni locali consente l'override degli utenti.</span><span class="sxs-lookup"><span data-stu-id="0aec5-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="0aec5-122">Per ulteriori informazioni, vedere [impostazioni locali \_ dell' \_ utente](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="0aec5-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aec5-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0aec5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aec5-124">Uso del supporto per le lingue nazionali</span><span class="sxs-lookup"><span data-stu-id="0aec5-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="0aec5-125">Impostazioni locali personalizzate</span><span class="sxs-lookup"><span data-stu-id="0aec5-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="0aec5-126">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="0aec5-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



