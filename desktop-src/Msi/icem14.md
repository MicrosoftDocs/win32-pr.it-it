---
description: ICEM14 convalida la colonna valore della tabella ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130447"
---
# <a name="icem14"></a><span data-ttu-id="3c138-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="3c138-103">ICEM14</span></span>

<span data-ttu-id="3c138-104">ICEM14 convalida la colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="3c138-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="3c138-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="3c138-105">Result</span></span>

<span data-ttu-id="3c138-106">ICEM14 invia i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="3c138-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="3c138-107">Errore</span><span class="sxs-lookup"><span data-stu-id="3c138-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="3c138-108">Significato</span><span class="sxs-lookup"><span data-stu-id="3c138-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c138-109">Stringa di sostituzione nella colonna ModuleSubstitution. Value nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] non è stato trovato nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c138-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="3c138-110">\[1 \] . \[ 2 \] . \[ 3 \] fa riferimento a una chiave primaria *Table. Row. Column* per una riga nella tabella ModuleSubstitution.</span><span class="sxs-lookup"><span data-stu-id="3c138-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="3c138-111">Il modello di formattazione nel campo valore di questa riga non corrisponde a una riga di attributi configurabili nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3c138-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="3c138-112">Nella tabella ModuleSubstitution nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] , nella tabella '% s'è indicato un elemento configurabile.</span><span class="sxs-lookup"><span data-stu-id="3c138-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="3c138-113">La tabella '% s'non deve contenere elementi configurabili.</span><span class="sxs-lookup"><span data-stu-id="3c138-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="3c138-114">Una delle tabelle seguenti è elencata nella colonna della tabella della tabella ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)o [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3c138-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="3c138-115">Queste tabelle non possono contenere campi configurabili.</span><span class="sxs-lookup"><span data-stu-id="3c138-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="3c138-116">Nella tabella ModuleSubstitution nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] , viene specificata una stringa di sostituzione vuota.</span><span class="sxs-lookup"><span data-stu-id="3c138-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="3c138-117">Il modello di formattazione nel campo valore di questa riga non corrisponde a una riga di attributi configurabili nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3c138-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="3c138-118">ICEM14 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="3c138-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="3c138-119">Avviso</span><span class="sxs-lookup"><span data-stu-id="3c138-119">Warning</span></span>                                                                  | <span data-ttu-id="3c138-120">Significato</span><span class="sxs-lookup"><span data-stu-id="3c138-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="3c138-121">La tabella ModuleSubstitution esiste ma manca la tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c138-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="3c138-122">La tabella ModuleConfiguration è assente.</span><span class="sxs-lookup"><span data-stu-id="3c138-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="3c138-123">Tabella utilizzata durante l'esecuzione</span><span class="sxs-lookup"><span data-stu-id="3c138-123">Table Used During Execution</span></span>

[<span data-ttu-id="3c138-124">Tabella ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="3c138-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="3c138-125">Tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c138-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="3c138-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c138-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c138-127">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="3c138-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



