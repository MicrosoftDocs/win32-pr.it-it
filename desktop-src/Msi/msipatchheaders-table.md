---
description: La tabella MsiPatchHeaders include i flussi di intestazione della patch binaria usati per la convalida delle patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabella MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231863"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="e21b6-103">Tabella MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="e21b6-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="e21b6-104">La tabella MsiPatchHeaders include i flussi di intestazione della patch binaria usati per la convalida delle patch.</span><span class="sxs-lookup"><span data-stu-id="e21b6-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="e21b6-105">La tabella MsiPatchHeaders viene utilizzata quando le chiavi della [tabella di file](file-table.md) lunghi generano un errore durante la generazione del flusso dell'intestazione patch nella [tabella patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="e21b6-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="e21b6-106">Questo problema può essere dovuto alla limitazione del nome del flusso descritta in [limitazioni OLE sui flussi](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e21b6-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="e21b6-107">In questo caso, la tabella delle patch può fare riferimento alla tabella MsiPatchHeaders per creare il flusso dell'intestazione della patch.</span><span class="sxs-lookup"><span data-stu-id="e21b6-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="e21b6-108">La tabella MsiPatchHeaders include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="e21b6-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="e21b6-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="e21b6-109">Column</span></span>    | <span data-ttu-id="e21b6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e21b6-110">Type</span></span>                         | <span data-ttu-id="e21b6-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="e21b6-111">Key</span></span> | <span data-ttu-id="e21b6-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="e21b6-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="e21b6-113">StreamRef</span><span class="sxs-lookup"><span data-stu-id="e21b6-113">StreamRef</span></span> | [<span data-ttu-id="e21b6-114">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e21b6-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="e21b6-115">S</span><span class="sxs-lookup"><span data-stu-id="e21b6-115">Y</span></span>   | <span data-ttu-id="e21b6-116">N</span><span class="sxs-lookup"><span data-stu-id="e21b6-116">N</span></span>        |
| <span data-ttu-id="e21b6-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e21b6-117">Header</span></span>    | [<span data-ttu-id="e21b6-118">Binario</span><span class="sxs-lookup"><span data-stu-id="e21b6-118">Binary</span></span>](binary.md)         | <span data-ttu-id="e21b6-119">N</span><span class="sxs-lookup"><span data-stu-id="e21b6-119">N</span></span>   | <span data-ttu-id="e21b6-120">N</span><span class="sxs-lookup"><span data-stu-id="e21b6-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e21b6-121">Colonne</span><span class="sxs-lookup"><span data-stu-id="e21b6-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e21b6-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span><span class="sxs-lookup"><span data-stu-id="e21b6-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="e21b6-123">Chiave primaria per la tabella che identifica in modo univoco una particolare intestazione patch.</span><span class="sxs-lookup"><span data-stu-id="e21b6-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="e21b6-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione</span><span class="sxs-lookup"><span data-stu-id="e21b6-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="e21b6-125">Questa colonna è l'intestazione patch del flusso binario utilizzata per la convalida delle patch.</span><span class="sxs-lookup"><span data-stu-id="e21b6-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e21b6-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="e21b6-126">Remarks</span></span>

<span data-ttu-id="e21b6-127">Questa tabella viene elaborata dall' [azione PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="e21b6-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="e21b6-128">Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="e21b6-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="e21b6-129">Non viene in genere creato direttamente in un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="e21b6-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="e21b6-130">Convalida</span><span class="sxs-lookup"><span data-stu-id="e21b6-130">Validation</span></span>

<dl>

[<span data-ttu-id="e21b6-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="e21b6-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e21b6-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="e21b6-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e21b6-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="e21b6-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



