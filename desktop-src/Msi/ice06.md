---
description: ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella \_ tabella di convalida siano presenti nella tabella. Se una tabella non esiste, eventuali \_ voci di convalida per tale tabella verranno ignorate.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967796"
---
# <a name="ice06"></a><span data-ttu-id="e7ce5-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="e7ce5-104">ICE06</span></span>

<span data-ttu-id="e7ce5-105">ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella [ \_ tabella di convalida](-validation-table.md) siano presenti nella tabella.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="e7ce5-106">Se una tabella non esiste, eventuali \_ voci di convalida per tale tabella verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="e7ce5-107">Lo scopo di ICE06 consiste nel rilevare le istanze in cui un autore tenta di utilizzare una nuova \_ tabella di convalida che riflette una modifica dello schema con un database obsoleto che non è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="e7ce5-108">ICE06 rileva inoltre il caso inverso di una \_ tabella di convalida precedente utilizzata con un database modificato.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="e7ce5-109">Si noti che la convalida interna eseguita da [ICE03](ice03.md) rileva l'istanza di una colonna di tabella non definita nella \_ tabella di convalida che viene elencata nel catalogo Columns.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="e7ce5-110">L'utilizzo di ICE03 e ICE06 garantisce pertanto la verifica di ogni colonna del database.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="e7ce5-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="e7ce5-111">Result</span></span>

<span data-ttu-id="e7ce5-112">ICE06 Invia un errore quando nella tabella di convalida è definita una colonna della tabella \_ che non è elencata nella \_ tabella Columns.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="e7ce5-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7ce5-113">Example</span></span>

<span data-ttu-id="e7ce5-114">Per l'esempio seguente ICE06 invia il messaggio</span><span class="sxs-lookup"><span data-stu-id="e7ce5-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="e7ce5-115">Column: versione della tabella: ModuleSignature non è definito nel database.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="e7ce5-116">[ \_ Tabella di convalida](-validation-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e7ce5-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="e7ce5-117">Tabella</span><span class="sxs-lookup"><span data-stu-id="e7ce5-117">Table</span></span>           | <span data-ttu-id="e7ce5-118">Colonna</span><span class="sxs-lookup"><span data-stu-id="e7ce5-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="e7ce5-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="e7ce5-119">ModuleSignature</span></span> | <span data-ttu-id="e7ce5-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="e7ce5-120">ModuleID</span></span> |
| <span data-ttu-id="e7ce5-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="e7ce5-121">ModuleSignature</span></span> | <span data-ttu-id="e7ce5-122">Versione</span><span class="sxs-lookup"><span data-stu-id="e7ce5-122">Version</span></span>  |



 

<span data-ttu-id="e7ce5-123">[ \_ Tabella Columns](-columns-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e7ce5-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="e7ce5-124">Tabella</span><span class="sxs-lookup"><span data-stu-id="e7ce5-124">Table</span></span>           | <span data-ttu-id="e7ce5-125">Number</span><span class="sxs-lookup"><span data-stu-id="e7ce5-125">Number</span></span> | <span data-ttu-id="e7ce5-126">Nome</span><span class="sxs-lookup"><span data-stu-id="e7ce5-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="e7ce5-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="e7ce5-127">ModuleSignature</span></span> | <span data-ttu-id="e7ce5-128">1</span><span class="sxs-lookup"><span data-stu-id="e7ce5-128">1</span></span>      | <span data-ttu-id="e7ce5-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="e7ce5-129">ModuleID</span></span> |



 

<span data-ttu-id="e7ce5-130">La colonna Version della tabella ModuleSignature non è presente nel database o è elencata nella \_ tabella Columns.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7ce5-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7ce5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7ce5-132">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e7ce5-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



