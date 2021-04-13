---
description: Sequenze di azioni suggerite per una tabella AdminExecuteSequence di base in un database Windows Installer.
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: AdminExecuteSequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ead890630b397062c6b8e645385b2810fa39d95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527025"
---
# <a name="suggested-adminexecutesequence"></a><span data-ttu-id="0841b-103">AdminExecuteSequence suggerito</span><span class="sxs-lookup"><span data-stu-id="0841b-103">Suggested AdminExecuteSequence</span></span>



| <span data-ttu-id="0841b-104">Azione</span><span class="sxs-lookup"><span data-stu-id="0841b-104">Action</span></span>                                                | <span data-ttu-id="0841b-105">Condizione</span><span class="sxs-lookup"><span data-stu-id="0841b-105">Condition</span></span> | <span data-ttu-id="0841b-106">Sequenza</span><span class="sxs-lookup"><span data-stu-id="0841b-106">Sequence</span></span> |
|-------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="0841b-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="0841b-107">CostInitialize</span></span>](costinitialize-action.md)           |           | <span data-ttu-id="0841b-108">800</span><span class="sxs-lookup"><span data-stu-id="0841b-108">800</span></span>      |
| [<span data-ttu-id="0841b-109">Filecost</span><span class="sxs-lookup"><span data-stu-id="0841b-109">FileCost</span></span>](filecost-action.md)                       |           | <span data-ttu-id="0841b-110">900</span><span class="sxs-lookup"><span data-stu-id="0841b-110">900</span></span>      |
| [<span data-ttu-id="0841b-111">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="0841b-111">CostFinalize</span></span>](costfinalize-action.md)               |           | <span data-ttu-id="0841b-112">1000</span><span class="sxs-lookup"><span data-stu-id="0841b-112">1000</span></span>     |
| [<span data-ttu-id="0841b-113">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="0841b-113">InstallValidate</span></span>](installvalidate-action.md)         |           | <span data-ttu-id="0841b-114">1400</span><span class="sxs-lookup"><span data-stu-id="0841b-114">1400</span></span>     |
| [<span data-ttu-id="0841b-115">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0841b-115">InstallInitialize</span></span>](installinitialize-action.md)     |           | <span data-ttu-id="0841b-116">1500</span><span class="sxs-lookup"><span data-stu-id="0841b-116">1500</span></span>     |
| [<span data-ttu-id="0841b-117">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="0841b-117">InstallAdminPackage</span></span>](installadminpackage-action.md) |           | <span data-ttu-id="0841b-118">3900</span><span class="sxs-lookup"><span data-stu-id="0841b-118">3900</span></span>     |
| [<span data-ttu-id="0841b-119">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="0841b-119">InstallFiles</span></span>](installfiles-action.md)               |           | <span data-ttu-id="0841b-120">4000</span><span class="sxs-lookup"><span data-stu-id="0841b-120">4000</span></span>     |
| [<span data-ttu-id="0841b-121">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="0841b-121">InstallFinalize</span></span>](installfinalize-action.md)         |           | <span data-ttu-id="0841b-122">6600</span><span class="sxs-lookup"><span data-stu-id="0841b-122">6600</span></span>     |



 

 

 



