---
description: La tabella binaria include i dati binari per elementi come bitmap, animazioni e icone. La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate. Vedere limitazioni OLE sui flussi.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabella binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311014"
---
# <a name="binary-table"></a><span data-ttu-id="3c641-105">Tabella binaria</span><span class="sxs-lookup"><span data-stu-id="3c641-105">Binary Table</span></span>

<span data-ttu-id="3c641-106">La tabella binaria include i dati binari per elementi come bitmap, animazioni e icone.</span><span class="sxs-lookup"><span data-stu-id="3c641-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="3c641-107">La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="3c641-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="3c641-108">Vedere [limitazioni OLE sui flussi](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3c641-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="3c641-109">La tabella binaria contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c641-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="3c641-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="3c641-110">Column</span></span> | <span data-ttu-id="3c641-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c641-111">Type</span></span>                         | <span data-ttu-id="3c641-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="3c641-112">Key</span></span> | <span data-ttu-id="3c641-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="3c641-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="3c641-114">Nome</span><span class="sxs-lookup"><span data-stu-id="3c641-114">Name</span></span>   | [<span data-ttu-id="3c641-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3c641-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="3c641-116">S</span><span class="sxs-lookup"><span data-stu-id="3c641-116">Y</span></span>   | <span data-ttu-id="3c641-117">N</span><span class="sxs-lookup"><span data-stu-id="3c641-117">N</span></span>        |
| <span data-ttu-id="3c641-118">Data</span><span class="sxs-lookup"><span data-stu-id="3c641-118">Data</span></span>   | [<span data-ttu-id="3c641-119">Binario</span><span class="sxs-lookup"><span data-stu-id="3c641-119">Binary</span></span>](binary.md)         | <span data-ttu-id="3c641-120">N</span><span class="sxs-lookup"><span data-stu-id="3c641-120">N</span></span>   | <span data-ttu-id="3c641-121">N</span><span class="sxs-lookup"><span data-stu-id="3c641-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3c641-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="3c641-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3c641-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="3c641-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3c641-124">Chiave univoca che identifica i dati binari specifici.</span><span class="sxs-lookup"><span data-stu-id="3c641-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="3c641-125">Se i dati binari sono per un controllo, la chiave viene visualizzata nella colonna di testo del controllo associato nella [tabella del controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="3c641-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="3c641-126">Questa chiave deve essere univoca tra tutti i controlli che richiedono dati binari.</span><span class="sxs-lookup"><span data-stu-id="3c641-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="3c641-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="3c641-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="3c641-128">Dati binari non formattati.</span><span class="sxs-lookup"><span data-stu-id="3c641-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="3c641-129">Convalida</span><span class="sxs-lookup"><span data-stu-id="3c641-129">Validation</span></span>

<dl>

[<span data-ttu-id="3c641-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="3c641-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3c641-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="3c641-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3c641-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="3c641-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="3c641-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="3c641-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



