---
description: Sequenze di azioni suggerite per una tabella AdvtExecuteSequence di base in un database Windows Installer.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: AdvtExecuteSequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319960"
---
# <a name="suggested-advtexecutesequence"></a><span data-ttu-id="7db3c-103">AdvtExecuteSequence suggerito</span><span class="sxs-lookup"><span data-stu-id="7db3c-103">Suggested AdvtExecuteSequence</span></span>



| <span data-ttu-id="7db3c-104">Azione</span><span class="sxs-lookup"><span data-stu-id="7db3c-104">Action</span></span>                                                    | <span data-ttu-id="7db3c-105">Condizione</span><span class="sxs-lookup"><span data-stu-id="7db3c-105">Condition</span></span> | <span data-ttu-id="7db3c-106">Sequenza</span><span class="sxs-lookup"><span data-stu-id="7db3c-106">Sequence</span></span> |
|-----------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="7db3c-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="7db3c-107">CostInitialize</span></span>](costinitialize-action.md)               |           | <span data-ttu-id="7db3c-108">800</span><span class="sxs-lookup"><span data-stu-id="7db3c-108">800</span></span>      |
| [<span data-ttu-id="7db3c-109">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="7db3c-109">CostFinalize</span></span>](costfinalize-action.md)                   |           | <span data-ttu-id="7db3c-110">1000</span><span class="sxs-lookup"><span data-stu-id="7db3c-110">1000</span></span>     |
| [<span data-ttu-id="7db3c-111">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="7db3c-111">InstallValidate</span></span>](installvalidate-action.md)             |           | <span data-ttu-id="7db3c-112">1400</span><span class="sxs-lookup"><span data-stu-id="7db3c-112">1400</span></span>     |
| [<span data-ttu-id="7db3c-113">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="7db3c-113">InstallInitialize</span></span>](installinitialize-action.md)         |           | <span data-ttu-id="7db3c-114">1500</span><span class="sxs-lookup"><span data-stu-id="7db3c-114">1500</span></span>     |
| [<span data-ttu-id="7db3c-115">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="7db3c-115">CreateShortcuts</span></span>](createshortcuts-action.md)             |           | <span data-ttu-id="7db3c-116">4500</span><span class="sxs-lookup"><span data-stu-id="7db3c-116">4500</span></span>     |
| [<span data-ttu-id="7db3c-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="7db3c-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)         |           | <span data-ttu-id="7db3c-118">4600</span><span class="sxs-lookup"><span data-stu-id="7db3c-118">4600</span></span>     |
| [<span data-ttu-id="7db3c-119">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="7db3c-119">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md) |           | <span data-ttu-id="7db3c-120">4700</span><span class="sxs-lookup"><span data-stu-id="7db3c-120">4700</span></span>     |
| [<span data-ttu-id="7db3c-121">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="7db3c-121">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)       |           | <span data-ttu-id="7db3c-122">4800</span><span class="sxs-lookup"><span data-stu-id="7db3c-122">4800</span></span>     |
| [<span data-ttu-id="7db3c-123">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="7db3c-123">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)           |           | <span data-ttu-id="7db3c-124">4900</span><span class="sxs-lookup"><span data-stu-id="7db3c-124">4900</span></span>     |
| [<span data-ttu-id="7db3c-125">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="7db3c-125">PublishComponents</span></span>](publishcomponents-action.md)         |           | <span data-ttu-id="7db3c-126">6200</span><span class="sxs-lookup"><span data-stu-id="7db3c-126">6200</span></span>     |
| [<span data-ttu-id="7db3c-127">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="7db3c-127">PublishFeatures</span></span>](publishfeatures-action.md)             |           | <span data-ttu-id="7db3c-128">6300</span><span class="sxs-lookup"><span data-stu-id="7db3c-128">6300</span></span>     |
| [<span data-ttu-id="7db3c-129">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="7db3c-129">PublishProduct</span></span>](publishproduct-action.md)               |           | <span data-ttu-id="7db3c-130">6400</span><span class="sxs-lookup"><span data-stu-id="7db3c-130">6400</span></span>     |
| [<span data-ttu-id="7db3c-131">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="7db3c-131">InstallFinalize</span></span>](installfinalize-action.md)             |           | <span data-ttu-id="7db3c-132">6600</span><span class="sxs-lookup"><span data-stu-id="7db3c-132">6600</span></span>     |



 

 

 



