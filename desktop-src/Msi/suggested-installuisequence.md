---
description: Sequenze di azioni suggerite per una tabella InstalUISequence di base in un database Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313329"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="45d9a-103">InstallUISequence suggerito</span><span class="sxs-lookup"><span data-stu-id="45d9a-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="45d9a-104">Azione</span><span class="sxs-lookup"><span data-stu-id="45d9a-104">Action</span></span>                                          | <span data-ttu-id="45d9a-105">Condizione</span><span class="sxs-lookup"><span data-stu-id="45d9a-105">Condition</span></span>                                                                                                  | <span data-ttu-id="45d9a-106">Sequenza</span><span class="sxs-lookup"><span data-stu-id="45d9a-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="45d9a-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="45d9a-108">-3</span><span class="sxs-lookup"><span data-stu-id="45d9a-108">-3</span></span>       |
| <span data-ttu-id="45d9a-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="45d9a-110">-2</span><span class="sxs-lookup"><span data-stu-id="45d9a-110">-2</span></span>       |
| <span data-ttu-id="45d9a-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="45d9a-112">-1</span><span class="sxs-lookup"><span data-stu-id="45d9a-112">-1</span></span>       |
| [<span data-ttu-id="45d9a-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="45d9a-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="45d9a-114">100</span><span class="sxs-lookup"><span data-stu-id="45d9a-114">100</span></span>      |
| <span data-ttu-id="45d9a-115">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="45d9a-116">140</span><span class="sxs-lookup"><span data-stu-id="45d9a-116">140</span></span>      |
| [<span data-ttu-id="45d9a-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="45d9a-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="45d9a-118">400</span><span class="sxs-lookup"><span data-stu-id="45d9a-118">400</span></span>      |
| [<span data-ttu-id="45d9a-119">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="45d9a-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="45d9a-120">NON [ **installato**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="45d9a-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="45d9a-121">500</span><span class="sxs-lookup"><span data-stu-id="45d9a-121">500</span></span>      |
| [<span data-ttu-id="45d9a-122">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="45d9a-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="45d9a-123">NON [ **installato**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="45d9a-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="45d9a-124">600</span><span class="sxs-lookup"><span data-stu-id="45d9a-124">600</span></span>      |
| [<span data-ttu-id="45d9a-125">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="45d9a-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="45d9a-126">800</span><span class="sxs-lookup"><span data-stu-id="45d9a-126">800</span></span>      |
| [<span data-ttu-id="45d9a-127">Filecost</span><span class="sxs-lookup"><span data-stu-id="45d9a-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="45d9a-128">900</span><span class="sxs-lookup"><span data-stu-id="45d9a-128">900</span></span>      |
| [<span data-ttu-id="45d9a-129">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="45d9a-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="45d9a-130">1000</span><span class="sxs-lookup"><span data-stu-id="45d9a-130">1000</span></span>     |
| <span data-ttu-id="45d9a-131">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="45d9a-132">NON [ **installato**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="45d9a-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="45d9a-133">1230</span><span class="sxs-lookup"><span data-stu-id="45d9a-133">1230</span></span>     |
| <span data-ttu-id="45d9a-134">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-134">ResumeDlg</span></span>                                       | <span data-ttu-id="45d9a-135">[**Installazione**](installed.md) completata E ( [**ripresa**](resume.md) o [**preselezione**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="45d9a-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="45d9a-136">1240</span><span class="sxs-lookup"><span data-stu-id="45d9a-136">1240</span></span>     |
| <span data-ttu-id="45d9a-137">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="45d9a-138">[**Installazione**](installed.md) completata E non [**Riprendi**](resume.md) e non [**preselezionato**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="45d9a-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="45d9a-139">1250</span><span class="sxs-lookup"><span data-stu-id="45d9a-139">1250</span></span>     |
| <span data-ttu-id="45d9a-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="45d9a-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="45d9a-141">1280</span><span class="sxs-lookup"><span data-stu-id="45d9a-141">1280</span></span>     |
| [<span data-ttu-id="45d9a-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="45d9a-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="45d9a-143">1300</span><span class="sxs-lookup"><span data-stu-id="45d9a-143">1300</span></span>     |



 

 

 



