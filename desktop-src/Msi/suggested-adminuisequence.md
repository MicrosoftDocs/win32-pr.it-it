---
description: Sequenze di azioni suggerite per una tabella AdminUISequence di base in un database Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755399"
---
# <a name="suggested-adminuisequence"></a><span data-ttu-id="eec6c-103">AdminUISequence suggerito</span><span class="sxs-lookup"><span data-stu-id="eec6c-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="eec6c-104">Azione</span><span class="sxs-lookup"><span data-stu-id="eec6c-104">Action</span></span>                                      | <span data-ttu-id="eec6c-105">Condizione</span><span class="sxs-lookup"><span data-stu-id="eec6c-105">Condition</span></span> | <span data-ttu-id="eec6c-106">Sequenza</span><span class="sxs-lookup"><span data-stu-id="eec6c-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="eec6c-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="eec6c-108">-3</span><span class="sxs-lookup"><span data-stu-id="eec6c-108">-3</span></span>       |
| <span data-ttu-id="eec6c-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="eec6c-110">-2</span><span class="sxs-lookup"><span data-stu-id="eec6c-110">-2</span></span>       |
| <span data-ttu-id="eec6c-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="eec6c-112">-1</span><span class="sxs-lookup"><span data-stu-id="eec6c-112">-1</span></span>       |
| <span data-ttu-id="eec6c-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="eec6c-114">140</span><span class="sxs-lookup"><span data-stu-id="eec6c-114">140</span></span>      |
| [<span data-ttu-id="eec6c-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="eec6c-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="eec6c-116">800</span><span class="sxs-lookup"><span data-stu-id="eec6c-116">800</span></span>      |
| [<span data-ttu-id="eec6c-117">Filecost</span><span class="sxs-lookup"><span data-stu-id="eec6c-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="eec6c-118">900</span><span class="sxs-lookup"><span data-stu-id="eec6c-118">900</span></span>      |
| [<span data-ttu-id="eec6c-119">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="eec6c-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="eec6c-120">1000</span><span class="sxs-lookup"><span data-stu-id="eec6c-120">1000</span></span>     |
| <span data-ttu-id="eec6c-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="eec6c-122">1230</span><span class="sxs-lookup"><span data-stu-id="eec6c-122">1230</span></span>     |
| <span data-ttu-id="eec6c-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="eec6c-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="eec6c-124">1280</span><span class="sxs-lookup"><span data-stu-id="eec6c-124">1280</span></span>     |
| [<span data-ttu-id="eec6c-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="eec6c-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="eec6c-126">1300</span><span class="sxs-lookup"><span data-stu-id="eec6c-126">1300</span></span>     |



 

 

 



