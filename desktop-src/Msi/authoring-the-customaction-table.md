---
description: Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella tabella CustomAction. Per ulteriori informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere azione personalizzata di tipo 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creazione della tabella CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967261"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="9fd8a-104">Creazione della tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="9fd8a-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="9fd8a-105">Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8a-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="9fd8a-106">Per ulteriori informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere [azione personalizzata di tipo 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8a-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="9fd8a-107">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="9fd8a-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="9fd8a-108">Azione</span><span class="sxs-lookup"><span data-stu-id="9fd8a-108">Action</span></span>            | <span data-ttu-id="9fd8a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fd8a-109">Type</span></span>  | <span data-ttu-id="9fd8a-110">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="9fd8a-110">Source</span></span>      | <span data-ttu-id="9fd8a-111">Destinazione</span><span class="sxs-lookup"><span data-stu-id="9fd8a-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="9fd8a-112">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="9fd8a-112">ProcessAccounts</span></span>   | <span data-ttu-id="9fd8a-113">1</span><span class="sxs-lookup"><span data-stu-id="9fd8a-113">1</span></span>     | <span data-ttu-id="9fd8a-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-114">Process.dll</span></span> | <span data-ttu-id="9fd8a-115">ProcessUserAccounts</span><span class="sxs-lookup"><span data-stu-id="9fd8a-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="9fd8a-116">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="9fd8a-116">UninstallAccounts</span></span> | <span data-ttu-id="9fd8a-117">1</span><span class="sxs-lookup"><span data-stu-id="9fd8a-117">1</span></span>     | <span data-ttu-id="9fd8a-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-118">Process.dll</span></span> | <span data-ttu-id="9fd8a-119">UninstallUserAccounts</span><span class="sxs-lookup"><span data-stu-id="9fd8a-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="9fd8a-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-120">CreateAccount</span></span>     | <span data-ttu-id="9fd8a-121">11265</span><span class="sxs-lookup"><span data-stu-id="9fd8a-121">11265</span></span> | <span data-ttu-id="9fd8a-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-122">Create.dll</span></span>  | <span data-ttu-id="9fd8a-123">CreateUserAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="9fd8a-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-124">RemoveAccount</span></span>     | <span data-ttu-id="9fd8a-125">11265</span><span class="sxs-lookup"><span data-stu-id="9fd8a-125">11265</span></span> | <span data-ttu-id="9fd8a-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-126">Remove.dll</span></span>  | <span data-ttu-id="9fd8a-127">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="9fd8a-128">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-128">RollbackAccount</span></span>   | <span data-ttu-id="9fd8a-129">9473</span><span class="sxs-lookup"><span data-stu-id="9fd8a-129">9473</span></span>  | <span data-ttu-id="9fd8a-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-130">Remove.dll</span></span>  | <span data-ttu-id="9fd8a-131">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="9fd8a-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="9fd8a-132">Il codice sorgente C++ per le librerie a collegamento dinamico è disponibile in Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="9fd8a-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="9fd8a-133">Usare Process. cpp per creare il file Process.dll.</span><span class="sxs-lookup"><span data-stu-id="9fd8a-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="9fd8a-134">Usare create. cpp per creare il file Create.dll.</span><span class="sxs-lookup"><span data-stu-id="9fd8a-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="9fd8a-135">Usare Remove. cpp per creare Remove.dll.</span><span class="sxs-lookup"><span data-stu-id="9fd8a-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="9fd8a-136">Aggiungere i file di libreria a collegamento dinamico alla tabella binaria.</span><span class="sxs-lookup"><span data-stu-id="9fd8a-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="9fd8a-137">Tabella binaria</span><span class="sxs-lookup"><span data-stu-id="9fd8a-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="9fd8a-138">Nome</span><span class="sxs-lookup"><span data-stu-id="9fd8a-138">Name</span></span>        | <span data-ttu-id="9fd8a-139">Data</span><span class="sxs-lookup"><span data-stu-id="9fd8a-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="9fd8a-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-140">Process.dll</span></span> | <span data-ttu-id="9fd8a-141">{*dati binari*}</span><span class="sxs-lookup"><span data-stu-id="9fd8a-141">{*binary data*}</span></span> |
| <span data-ttu-id="9fd8a-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-142">Create.dll</span></span>  | <span data-ttu-id="9fd8a-143">{*dati binari*}</span><span class="sxs-lookup"><span data-stu-id="9fd8a-143">{*binary data*}</span></span> |
| <span data-ttu-id="9fd8a-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="9fd8a-144">Remove.dll</span></span>  | <span data-ttu-id="9fd8a-145">{*dati binari*}</span><span class="sxs-lookup"><span data-stu-id="9fd8a-145">{*binary data*}</span></span> |



 

<span data-ttu-id="9fd8a-146">Continuare ad [aggiungere una tabella CustomUserAccounts personalizzata](adding-a-custom-customuseraccounts-table.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8a-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



