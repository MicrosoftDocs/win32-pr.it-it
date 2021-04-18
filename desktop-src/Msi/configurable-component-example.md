---
description: Questo esempio consente al consumer del modulo di configurare in modo indipendente un controllo di modifica, l'attributo checksum e l'attributo compresso.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Esempio di componente configurabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308198"
---
# <a name="configurable-component-example"></a><span data-ttu-id="c795f-103">Esempio di componente configurabile</span><span class="sxs-lookup"><span data-stu-id="c795f-103">Configurable Component Example</span></span>

<span data-ttu-id="c795f-104">In questo esempio, le tabelle ModuleConfiguration e ModuleSubstitution seguenti consentono al consumer del modulo di configurare in modo indipendente l'attributo password per un controllo di modifica, l'attributo checksum per un file e l'attributo compresso per lo stesso file.</span><span class="sxs-lookup"><span data-stu-id="c795f-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="c795f-105">Tabella ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="c795f-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="c795f-106">Tabella</span><span class="sxs-lookup"><span data-stu-id="c795f-106">Table</span></span>   | <span data-ttu-id="c795f-107">Riga</span><span class="sxs-lookup"><span data-stu-id="c795f-107">Row</span></span>           | <span data-ttu-id="c795f-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="c795f-108">Column</span></span>     | <span data-ttu-id="c795f-109">valore</span><span class="sxs-lookup"><span data-stu-id="c795f-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="c795f-110">Control</span><span class="sxs-lookup"><span data-stu-id="c795f-110">Control</span></span> | <span data-ttu-id="c795f-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="c795f-111">Dialog1;Edit1</span></span> | <span data-ttu-id="c795f-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="c795f-112">Attributes</span></span> | <span data-ttu-id="c795f-113">\[= Password\]</span><span class="sxs-lookup"><span data-stu-id="c795f-113">\[=Password\]</span></span>                |
| <span data-ttu-id="c795f-114">File</span><span class="sxs-lookup"><span data-stu-id="c795f-114">File</span></span>    | <span data-ttu-id="c795f-115">File1</span><span class="sxs-lookup"><span data-stu-id="c795f-115">File1</span></span>         | <span data-ttu-id="c795f-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="c795f-116">Attributes</span></span> | <span data-ttu-id="c795f-117">\[= Checksum \] \[ = compresso\]</span><span class="sxs-lookup"><span data-stu-id="c795f-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="c795f-118">Tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c795f-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="c795f-119">Nome</span><span class="sxs-lookup"><span data-stu-id="c795f-119">Name</span></span>       | <span data-ttu-id="c795f-120">Formato</span><span class="sxs-lookup"><span data-stu-id="c795f-120">Format</span></span>   | <span data-ttu-id="c795f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c795f-121">Type</span></span> | <span data-ttu-id="c795f-122">ContextData</span><span class="sxs-lookup"><span data-stu-id="c795f-122">ContextData</span></span>                              | <span data-ttu-id="c795f-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c795f-123">DefaultValue</span></span> | <span data-ttu-id="c795f-124">Attributi</span><span class="sxs-lookup"><span data-stu-id="c795f-124">Attributes</span></span> | <span data-ttu-id="c795f-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c795f-125">DisplayName</span></span> | <span data-ttu-id="c795f-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c795f-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="c795f-127">Password</span><span class="sxs-lookup"><span data-stu-id="c795f-127">Password</span></span>   | <span data-ttu-id="c795f-128">Bit</span><span class="sxs-lookup"><span data-stu-id="c795f-128">Bitfield</span></span> |      | <span data-ttu-id="c795f-129">2097152; True = 2097152; False = 0</span><span class="sxs-lookup"><span data-stu-id="c795f-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="c795f-130">0</span><span class="sxs-lookup"><span data-stu-id="c795f-130">0</span></span>            | <span data-ttu-id="c795f-131">0</span><span class="sxs-lookup"><span data-stu-id="c795f-131">0</span></span>          |             |             |
| <span data-ttu-id="c795f-132">Checksum</span><span class="sxs-lookup"><span data-stu-id="c795f-132">Checksum</span></span>   | <span data-ttu-id="c795f-133">Bit</span><span class="sxs-lookup"><span data-stu-id="c795f-133">Bitfield</span></span> |      | <span data-ttu-id="c795f-134">1024; Checksum = 1024; Nessun checksum = 0</span><span class="sxs-lookup"><span data-stu-id="c795f-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="c795f-135">0</span><span class="sxs-lookup"><span data-stu-id="c795f-135">0</span></span>            | <span data-ttu-id="c795f-136">0</span><span class="sxs-lookup"><span data-stu-id="c795f-136">0</span></span>          |             |             |
| <span data-ttu-id="c795f-137">Compresso</span><span class="sxs-lookup"><span data-stu-id="c795f-137">Compressed</span></span> | <span data-ttu-id="c795f-138">Bit</span><span class="sxs-lookup"><span data-stu-id="c795f-138">Bitfield</span></span> |      | <span data-ttu-id="c795f-139">24576; Compressi = 16384; Non compresso = 8192</span><span class="sxs-lookup"><span data-stu-id="c795f-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="c795f-140">8192</span><span class="sxs-lookup"><span data-stu-id="c795f-140">8192</span></span>         | <span data-ttu-id="c795f-141">0</span><span class="sxs-lookup"><span data-stu-id="c795f-141">0</span></span>          |             |             |



 

 

 



