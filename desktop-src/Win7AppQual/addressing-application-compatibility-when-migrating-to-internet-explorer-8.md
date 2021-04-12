---
description: .
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab869be07e5578d265db2e8e85147c213e1e17e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233999"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="d962e-103">Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="d962e-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="d962e-104">In questa sezione viene fornita una panoramica del test dei problemi di compatibilità delle applicazioni e della risoluzione di tali problemi nelle applicazioni Web per Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="d962e-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="d962e-105">Negli argomenti seguenti vengono descritte le modifiche apportate a Internet Explorer 8 e agli strumenti e alle tecnologie per garantire la compatibilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d962e-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="d962e-106">Sezione</span><span class="sxs-lookup"><span data-stu-id="d962e-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="d962e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d962e-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d962e-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d962e-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="d962e-109">Viene fornita una panoramica delle considerazioni sulla compatibilità di Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="d962e-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="d962e-110">Informazioni sulla compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="d962e-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="d962e-111">Fornisce informazioni di base sulla compatibilità di Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="d962e-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="d962e-112">Standard Web e compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="d962e-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="d962e-113">Fornisce informazioni di base sui motivi per cui gli standard Web sono importanti.</span><span class="sxs-lookup"><span data-stu-id="d962e-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="d962e-114">Aggiornamenti della progettazione che incidono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="d962e-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="d962e-115">Fornisce informazioni sull'argomento sugli aggiornamenti della progettazione che incidono sulla compatibilità.</span><span class="sxs-lookup"><span data-stu-id="d962e-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="d962e-116">Correzione dei problemi di compatibilità nelle applicazioni Web e nei componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d962e-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="d962e-117">Offre suggerimenti per risolvere i problemi di compatibilità con le applicazioni Web e i componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d962e-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="d962e-118">Strumenti per il debug di applicazioni Web e componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d962e-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="d962e-119">Elenca gli strumenti disponibili per il debug di applicazioni Web e componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d962e-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="d962e-120">Appendice 1: modifiche del browser da Internet Explorer 6 a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="d962e-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="d962e-121">Elenca le modifiche apportate da Microsoft Internet Explorer 6 a Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="d962e-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="d962e-122">Appendice 2: scenari di script di test</span><span class="sxs-lookup"><span data-stu-id="d962e-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="d962e-123">Elenca gli scenari consigliati per il test dei siti per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="d962e-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



