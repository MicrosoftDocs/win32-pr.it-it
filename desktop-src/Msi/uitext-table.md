---
description: La tabella UIText contiene le versioni localizzate di alcune stringhe utilizzate nell'interfaccia utente. Queste stringhe non fanno parte di nessun'altra tabella. La tabella UIText è per le stringhe che non dispongono di una posizione logica in nessun'altra tabella.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabella UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128099"
---
# <a name="uitext-table"></a><span data-ttu-id="081bf-105">Tabella UIText</span><span class="sxs-lookup"><span data-stu-id="081bf-105">UIText Table</span></span>

<span data-ttu-id="081bf-106">La tabella UIText contiene le versioni localizzate di alcune stringhe utilizzate nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="081bf-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="081bf-107">Queste stringhe non fanno parte di nessun'altra tabella.</span><span class="sxs-lookup"><span data-stu-id="081bf-107">These strings are not part of any other table.</span></span> <span data-ttu-id="081bf-108">La tabella UIText è per le stringhe che non dispongono di una posizione logica in nessun'altra tabella.</span><span class="sxs-lookup"><span data-stu-id="081bf-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="081bf-109">La tabella UIText include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="081bf-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="081bf-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="081bf-110">Column</span></span> | <span data-ttu-id="081bf-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="081bf-111">Type</span></span>                         | <span data-ttu-id="081bf-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="081bf-112">Key</span></span> | <span data-ttu-id="081bf-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="081bf-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="081bf-114">Chiave</span><span class="sxs-lookup"><span data-stu-id="081bf-114">Key</span></span>    | [<span data-ttu-id="081bf-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="081bf-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="081bf-116">S</span><span class="sxs-lookup"><span data-stu-id="081bf-116">Y</span></span>   | <span data-ttu-id="081bf-117">N</span><span class="sxs-lookup"><span data-stu-id="081bf-117">N</span></span>        |
| <span data-ttu-id="081bf-118">Testo</span><span class="sxs-lookup"><span data-stu-id="081bf-118">Text</span></span>   | [<span data-ttu-id="081bf-119">Text</span><span class="sxs-lookup"><span data-stu-id="081bf-119">Text</span></span>](text.md)             | <span data-ttu-id="081bf-120">N</span><span class="sxs-lookup"><span data-stu-id="081bf-120">N</span></span>   | <span data-ttu-id="081bf-121">S</span><span class="sxs-lookup"><span data-stu-id="081bf-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="081bf-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="081bf-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="081bf-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="081bf-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="081bf-124">Chiave univoca che identifica la stringa particolare.</span><span class="sxs-lookup"><span data-stu-id="081bf-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="081bf-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo</span><span class="sxs-lookup"><span data-stu-id="081bf-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="081bf-126">Versione localizzata della stringa.</span><span class="sxs-lookup"><span data-stu-id="081bf-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="081bf-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="081bf-127">Remarks</span></span>

<span data-ttu-id="081bf-128">Alcuni controlli utilizzano la tabella UIText come origine delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="081bf-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="081bf-129">Per informazioni sulle stringhe richieste in questa tabella per ogni particolare controllo, vedere i singoli controlli nella Guida di [riferimento all'interfaccia utente](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="081bf-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="081bf-130">Convalida</span><span class="sxs-lookup"><span data-stu-id="081bf-130">Validation</span></span>

<dl>

[<span data-ttu-id="081bf-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="081bf-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="081bf-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="081bf-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



