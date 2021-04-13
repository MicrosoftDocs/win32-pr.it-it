---
description: Gli oggetti COMAdmin offrono un semplice modello a oggetti che consente di accedere al catalogo COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Panoramica degli oggetti COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127790"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="60c40-103">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="60c40-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="60c40-104">Gli oggetti COMAdmin offrono un semplice modello a oggetti che consente di accedere al catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="60c40-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="60c40-105">In questo modo, vengono utilizzati per modellare tutte le funzionalità fornite dallo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="60c40-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="60c40-106">Ogni volta che si esegue qualsiasi tipo di amministrazione COM+, si interagisce con il catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="60c40-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="60c40-107">Per una descrizione del catalogo, vedere [accesso al catalogo com+](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="60c40-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="60c40-108">Le informazioni ottenute dallo strumento di amministrazione Servizi componenti o utilizzando gli oggetti COMAdmin sono strutturate in modo analogo e le azioni eseguite in entrambi i contesti sono analoghe.</span><span class="sxs-lookup"><span data-stu-id="60c40-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="60c40-109">La correlazione di base tra l'utilizzo dello snap-in Servizi componenti e l'amministrazione a livello di codice è che le cartelle nell'albero della console dello snap-in corrispondono alle raccolte nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="60c40-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="60c40-110">Ovvero, così come ogni cartella nello snap-in contiene tutti gli elementi di un tipo; ad esempio, **le applicazioni com+** contengono applicazioni COM+ installate. ogni raccolta nel catalogo com+ include gli elementi di un tipo uniforme.</span><span class="sxs-lookup"><span data-stu-id="60c40-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="60c40-111">Inoltre, proprio come ogni elemento in una cartella include proprietà che è possibile impostare in una finestra delle proprietà, ogni elemento di una raccolta espone le proprietà che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="60c40-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="60c40-112">Per consentire la configurazione di oggetti all'interno di questa struttura, gli oggetti COMAdmin forniscono i mezzi per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="60c40-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="60c40-113">Accedere al catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="60c40-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="60c40-114">Accedere alle raccolte nel catalogo</span><span class="sxs-lookup"><span data-stu-id="60c40-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="60c40-115">Accedere agli elementi nelle raccolte</span><span class="sxs-lookup"><span data-stu-id="60c40-115">Access items in collections</span></span>
-   <span data-ttu-id="60c40-116">Accedere alle proprietà degli elementi nelle raccolte</span><span class="sxs-lookup"><span data-stu-id="60c40-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="60c40-117">Per supportare queste azioni, la libreria COMAdmin fornisce le tre classi seguenti:</span><span class="sxs-lookup"><span data-stu-id="60c40-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="60c40-118">[**COMAdminCatalog**](comadmincatalog.md), che rappresenta il catalogo stesso.</span><span class="sxs-lookup"><span data-stu-id="60c40-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="60c40-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), che rappresenta qualsiasi raccolta.</span><span class="sxs-lookup"><span data-stu-id="60c40-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="60c40-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), che rappresenta qualsiasi elemento in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="60c40-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="60c40-121">Per descrizioni più complete di queste classi, vedere [la descrizione riepilogativa delle classi COMAdmin](summary-description-of-the-comadmin-classes.md) in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="60c40-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="60c40-122">Per una rapida idea delle azioni tipiche eseguite nell'amministrazione a livello di codice, vedere [l'esempio introduttivo relativo all'uso del catalogo di amministrazione com+](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="60c40-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60c40-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60c40-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60c40-124">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="60c40-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="60c40-125">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="60c40-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="60c40-126">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="60c40-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="60c40-127">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="60c40-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="60c40-128">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="60c40-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



