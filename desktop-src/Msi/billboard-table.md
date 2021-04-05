---
description: Nella tabella Billboard sono elencati i controlli dei tabelloni visualizzati nell'interfaccia utente completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabella Billboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967256"
---
# <a name="billboard-table"></a><span data-ttu-id="f2e62-103">Tabella Billboard</span><span class="sxs-lookup"><span data-stu-id="f2e62-103">Billboard Table</span></span>

<span data-ttu-id="f2e62-104">Nella tabella Billboard sono elencati i [controlli dei tabelloni](billboard-control.md) visualizzati nell'interfaccia utente completa.</span><span class="sxs-lookup"><span data-stu-id="f2e62-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="f2e62-105">La tabella Billboard contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2e62-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="f2e62-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="f2e62-106">Column</span></span>    | <span data-ttu-id="f2e62-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2e62-107">Type</span></span>                         | <span data-ttu-id="f2e62-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="f2e62-108">Key</span></span> | <span data-ttu-id="f2e62-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f2e62-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="f2e62-110">Billboard</span><span class="sxs-lookup"><span data-stu-id="f2e62-110">Billboard</span></span> | [<span data-ttu-id="f2e62-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="f2e62-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2e62-112">S</span><span class="sxs-lookup"><span data-stu-id="f2e62-112">Y</span></span>   | <span data-ttu-id="f2e62-113">N</span><span class="sxs-lookup"><span data-stu-id="f2e62-113">N</span></span>        |
| <span data-ttu-id="f2e62-114">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="f2e62-114">Feature\_</span></span> | [<span data-ttu-id="f2e62-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="f2e62-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2e62-116">N</span><span class="sxs-lookup"><span data-stu-id="f2e62-116">N</span></span>   | <span data-ttu-id="f2e62-117">N</span><span class="sxs-lookup"><span data-stu-id="f2e62-117">N</span></span>        |
| <span data-ttu-id="f2e62-118">Azione</span><span class="sxs-lookup"><span data-stu-id="f2e62-118">Action</span></span>    | [<span data-ttu-id="f2e62-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="f2e62-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2e62-120">N</span><span class="sxs-lookup"><span data-stu-id="f2e62-120">N</span></span>   | <span data-ttu-id="f2e62-121">S</span><span class="sxs-lookup"><span data-stu-id="f2e62-121">Y</span></span>        |
| <span data-ttu-id="f2e62-122">Ordering</span><span class="sxs-lookup"><span data-stu-id="f2e62-122">Ordering</span></span>  | [<span data-ttu-id="f2e62-123">Integer</span><span class="sxs-lookup"><span data-stu-id="f2e62-123">Integer</span></span>](integer.md)       | <span data-ttu-id="f2e62-124">N</span><span class="sxs-lookup"><span data-stu-id="f2e62-124">N</span></span>   | <span data-ttu-id="f2e62-125">S</span><span class="sxs-lookup"><span data-stu-id="f2e62-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f2e62-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="f2e62-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f2e62-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span><span class="sxs-lookup"><span data-stu-id="f2e62-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-128">Nome del [controllo Billboard](billboard-control.md).</span><span class="sxs-lookup"><span data-stu-id="f2e62-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2e62-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="f2e62-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-130">Chiave esterna per la prima colonna della tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2e62-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="f2e62-131">Il tabellone viene visualizzato solo se questa funzionalità è in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="f2e62-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="f2e62-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="f2e62-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-133">Nome di un'azione.</span><span class="sxs-lookup"><span data-stu-id="f2e62-133">The name of an action.</span></span> <span data-ttu-id="f2e62-134">Il tabellone viene visualizzato durante i messaggi di stato ricevuti da questa azione.</span><span class="sxs-lookup"><span data-stu-id="f2e62-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="f2e62-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordinare</span><span class="sxs-lookup"><span data-stu-id="f2e62-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-136">Se è presente più di un Billboard corrispondente a un'azione, questi vengono visualizzati nell'ordine definito da questa colonna.</span><span class="sxs-lookup"><span data-stu-id="f2e62-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="f2e62-137">Questo numero deve essere non negativo.</span><span class="sxs-lookup"><span data-stu-id="f2e62-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="f2e62-138">Convalida</span><span class="sxs-lookup"><span data-stu-id="f2e62-138">Validation</span></span>

<dl>

[<span data-ttu-id="f2e62-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="f2e62-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f2e62-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="f2e62-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f2e62-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="f2e62-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f2e62-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="f2e62-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



