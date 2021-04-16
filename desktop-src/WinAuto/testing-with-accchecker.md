---
title: Test con AccChecker
description: Descrive il flusso di lavoro di test tipico che incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- test con AccChecker
- AccChecker, test del flusso di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515523"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="666cd-105">Test con AccChecker</span><span class="sxs-lookup"><span data-stu-id="666cd-105">Testing with AccChecker</span></span>

<span data-ttu-id="666cd-106">Nello scenario seguente vengono descritti i passaggi che si seguono in genere durante il test con AccChecker.</span><span class="sxs-lookup"><span data-stu-id="666cd-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="666cd-107">Quando le routine di verifica AccChecker sono in esecuzione, l'interazione dell'utente con il computer host può interferire con alcune routine.</span><span class="sxs-lookup"><span data-stu-id="666cd-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="666cd-108">Si consiglia di non eseguire ulteriori interazioni da parte dell'utente fino a quando AccChecker non notifica all'utente che tutte le attività sono state completate.</span><span class="sxs-lookup"><span data-stu-id="666cd-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="666cd-109">Eseguire le verifiche AccChecker su un'applicazione o un controllo di destinazione specifico.</span><span class="sxs-lookup"><span data-stu-id="666cd-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="666cd-110">Per ulteriori informazioni, vedere la [scheda verifiche](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="666cd-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="666cd-111">AccChecker non Esplora tutte le permutazioni dell'interfaccia utente in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="666cd-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="666cd-112">Gli elementi nascosti all'interno di controlli quali Windows, i riquadri, le schede e i menu devono essere esposti manualmente.</span><span class="sxs-lookup"><span data-stu-id="666cd-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="666cd-113">Esaminare il log degli errori di AccChecker e valutare o valutare i risultati.</span><span class="sxs-lookup"><span data-stu-id="666cd-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="666cd-114">Risolvere i problemi semplici e registrare i bug gravi nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="666cd-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="666cd-115">Genera un file di eliminazione per bug ed errori che possono essere ignorati fino al test di regressione.</span><span class="sxs-lookup"><span data-stu-id="666cd-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="666cd-116">Eseguire di nuovo le verifiche AccChecker con il file di eliminazione e le correzioni di bug iniziali.</span><span class="sxs-lookup"><span data-stu-id="666cd-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="666cd-117">Questo fornisce uno snapshot dei problemi nell'implementazione corrente di Microsoft Active Accessibility e stabilisce una baseline per i test di regressione.</span><span class="sxs-lookup"><span data-stu-id="666cd-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="666cd-118">Integrare le API AccChecker e il file di eliminazione in un Framework di test automatico per i test di regressione sui bug registrati dalle verifiche AccChecker iniziali.</span><span class="sxs-lookup"><span data-stu-id="666cd-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="666cd-119">Con la correzione dei bug, il file di eliminazione deve essere modificato in modo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="666cd-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="666cd-120">Verificare che non siano state introdotte regressioni o nuovi bug di accessibilità nell'applicazione o nel controllo.</span><span class="sxs-lookup"><span data-stu-id="666cd-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="666cd-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="666cd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="666cd-122">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="666cd-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




