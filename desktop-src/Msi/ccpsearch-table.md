---
description: La tabella CCPSearch contiene l'elenco delle firme di file utilizzate per il programma di verifica della conformità (CCP). È necessario che almeno uno di questi file sia presente nel computer di un utente affinché l'utente sia conforme al programma.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabella CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310997"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="d25a9-104">Tabella CCPSearch</span><span class="sxs-lookup"><span data-stu-id="d25a9-104">CCPSearch Table</span></span>

<span data-ttu-id="d25a9-105">La tabella CCPSearch contiene l'elenco delle firme di file utilizzate per il programma di verifica della conformità (CCP).</span><span class="sxs-lookup"><span data-stu-id="d25a9-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="d25a9-106">È necessario che almeno uno di questi file sia presente nel computer di un utente affinché l'utente sia conforme al programma.</span><span class="sxs-lookup"><span data-stu-id="d25a9-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="d25a9-107">La tabella CCPSearch include la colonna seguente.</span><span class="sxs-lookup"><span data-stu-id="d25a9-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="d25a9-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="d25a9-108">Column</span></span>      | <span data-ttu-id="d25a9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d25a9-109">Type</span></span>                         | <span data-ttu-id="d25a9-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="d25a9-110">Key</span></span> | <span data-ttu-id="d25a9-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d25a9-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d25a9-112">Firma\_</span><span class="sxs-lookup"><span data-stu-id="d25a9-112">Signature\_</span></span> | [<span data-ttu-id="d25a9-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d25a9-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d25a9-114">S</span><span class="sxs-lookup"><span data-stu-id="d25a9-114">Y</span></span>   | <span data-ttu-id="d25a9-115">N</span><span class="sxs-lookup"><span data-stu-id="d25a9-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="d25a9-116">Colonna</span><span class="sxs-lookup"><span data-stu-id="d25a9-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="d25a9-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="d25a9-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="d25a9-118">La firma \_ rappresenta una firma del file univoca ed è anche la chiave esterna nelle tabelle [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d25a9-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d25a9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d25a9-119">Remarks</span></span>

<span data-ttu-id="d25a9-120">Questa tabella viene definita quando viene eseguita l'azione [CCPSearch](ccpsearch-action.md) o [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d25a9-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="d25a9-121">Convalida</span><span class="sxs-lookup"><span data-stu-id="d25a9-121">Validation</span></span>

<dl>

[<span data-ttu-id="d25a9-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="d25a9-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d25a9-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="d25a9-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d25a9-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="d25a9-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



