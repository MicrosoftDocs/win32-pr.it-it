---
description: Windows Search USA risorse di lingua quali Word breaker e stemmer per suddividere il testo nelle impostazioni locali native durante la creazione dell'indice e l'elaborazione delle query.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Estensione delle risorse della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306103"
---
# <a name="extending-language-resources"></a><span data-ttu-id="c3e17-103">Estensione delle risorse della lingua</span><span class="sxs-lookup"><span data-stu-id="c3e17-103">Extending Language Resources</span></span>

<span data-ttu-id="c3e17-104">Windows Search USA risorse di lingua quali Word breaker e stemmer per suddividere il testo nelle impostazioni locali native durante la creazione dell'indice e l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="c3e17-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="c3e17-105">Microsoft fornisce Word breaker e stemmer per diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="c3e17-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="c3e17-106">In questa sezione viene descritto come implementare e utilizzare Word breaker e stemmer personalizzati per le lingue e le impostazioni locali oltre a quelle fornite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c3e17-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="c3e17-107">Informazioni sui componenti delle risorse della lingua</span><span class="sxs-lookup"><span data-stu-id="c3e17-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="c3e17-108">Implementazione di un Word breaker e uno stemmer</span><span class="sxs-lookup"><span data-stu-id="c3e17-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="c3e17-109">Considerazioni linguistiche e Unicode</span><span class="sxs-lookup"><span data-stu-id="c3e17-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="c3e17-110">Risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="c3e17-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="c3e17-111">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="c3e17-111">Additional Resources</span></span>

-   <span data-ttu-id="c3e17-112">Per un elenco di Lanuages supportati da Word breaker, vedere [linguaggi supportati da Windows Search](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="c3e17-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="c3e17-113">Se è necessario identificare la lingua di un testo, è possibile usare il rilevamento automatico del linguaggio (LAD), disponibile in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c3e17-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="c3e17-114">Per ulteriori informazioni, vedere [servizi linguistici estesi](../intl/extended-linguistic-services.md) (ELS).</span><span class="sxs-lookup"><span data-stu-id="c3e17-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="c3e17-115">Per la documentazione di riferimento applicabile, vedere [interfacce di componenti aggiuntivi per i dati](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="c3e17-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3e17-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3e17-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3e17-117">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="c3e17-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="c3e17-118">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="c3e17-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="c3e17-119">Estensione dell'indice</span><span class="sxs-lookup"><span data-stu-id="c3e17-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
