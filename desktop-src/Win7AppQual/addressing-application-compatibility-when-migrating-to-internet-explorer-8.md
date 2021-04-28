---
description: Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088769"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="9eeba-103">Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="9eeba-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="9eeba-104">Questa sezione offre una panoramica dei test per i problemi di compatibilità delle applicazioni e la risoluzione di tali problemi nelle applicazioni Web per Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9eeba-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="9eeba-105">Negli argomenti seguenti vengono descritte le modifiche apportate Internet Explorer 8 e gli strumenti e le tecnologie per garantire la compatibilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9eeba-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="9eeba-106">Sezione</span><span class="sxs-lookup"><span data-stu-id="9eeba-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="9eeba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eeba-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eeba-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="9eeba-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="9eeba-109">Offre una panoramica delle considerazioni sulla compatibilità Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9eeba-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="9eeba-110">Informazioni sulla compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="9eeba-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="9eeba-111">Fornisce informazioni di base sulla Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9eeba-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="9eeba-112">Standard Web e compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="9eeba-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="9eeba-113">Fornisce informazioni di base sui motivi per cui gli standard Web sono importanti.</span><span class="sxs-lookup"><span data-stu-id="9eeba-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="9eeba-114">Aggiornamenti della progettazione che influiscono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="9eeba-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="9eeba-115">Vengono fornite informazioni di argomento sugli aggiornamenti della progettazione che influiscono sulla compatibilità.</span><span class="sxs-lookup"><span data-stu-id="9eeba-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="9eeba-116">Correzione dei problemi di compatibilità nelle applicazioni Web e nei componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9eeba-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="9eeba-117">Offre suggerimenti per risolvere i problemi di compatibilità con applicazioni Web e componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9eeba-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="9eeba-118">Strumenti per il debug di applicazioni Web e componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9eeba-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="9eeba-119">Elenca gli strumenti disponibili per il debug di applicazioni Web e componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9eeba-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="9eeba-120">Appendice 1: da Internet Explorer 6 a Internet Explorer 8 modifiche del browser</span><span class="sxs-lookup"><span data-stu-id="9eeba-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="9eeba-121">Elenca le modifiche da Microsoft Internet Explorer 6 a Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9eeba-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="9eeba-122">Appendice 2: Scenari di script di test</span><span class="sxs-lookup"><span data-stu-id="9eeba-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="9eeba-123">Elenca gli scenari consigliati per i siti di test per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="9eeba-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



