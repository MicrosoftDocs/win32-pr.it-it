---
description: ICE76 verifica l'utilizzo del catalogo SFP (WFP) all'interno di Windows Installer pacchetti per Windows me. Questo ghiaccio verifica anche che nessun file nella tabella azione BindImage sul faccia riferimento a cataloghi SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308191"
---
# <a name="ice76"></a><span data-ttu-id="85138-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="85138-104">ICE76</span></span>

<span data-ttu-id="85138-105">ICE76 verifica l'utilizzo del catalogo SFP (WFP) all'interno di Windows Installer pacchetti per Windows me.</span><span class="sxs-lookup"><span data-stu-id="85138-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="85138-106">Questo ghiaccio verifica anche che nessun file nella [tabella](bindimage-table.md) azione BindImage sul faccia riferimento a cataloghi SFP.</span><span class="sxs-lookup"><span data-stu-id="85138-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="85138-107">La protezione dei file di Windows richiede una corrispondenza esatta tra il file e la firma incorporata nel file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="85138-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="85138-108">I file che fanno riferimento a un catalogo SFP non devono essere elencati nella tabella azione BindImage sul perché l'effetto dell' [azione azione BindImage sul](bindimage-action.md) su questi file è diverso tra i computer.</span><span class="sxs-lookup"><span data-stu-id="85138-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="85138-109">I file a cui fanno riferimento i cataloghi SFP devono trovarsi in componenti permanenti o installati localmente.</span><span class="sxs-lookup"><span data-stu-id="85138-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="85138-110">Risultato</span><span class="sxs-lookup"><span data-stu-id="85138-110">Result</span></span>

<span data-ttu-id="85138-111">ICE76 Invia un errore per ogni file nella [tabella azione BindImage sul](bindimage-table.md) presente anche nella [tabella FileSFPCatalog](filesfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="85138-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="85138-112">ICE76 genera un errore se un file nella tabella FileSFPCatalog appartiene a un componente con una delle seguenti condizioni:</span><span class="sxs-lookup"><span data-stu-id="85138-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="85138-113">**msidbComponentAttributesPermanent** non è impostato nella colonna Attributes della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="85138-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="85138-114">**msidbComponentAttributesSourceOnly** viene impostato nella colonna Attributes della tabella Component.</span><span class="sxs-lookup"><span data-stu-id="85138-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="85138-115">**msidbAttributesOptional** viene impostato nella colonna Attributes della tabella Component.</span><span class="sxs-lookup"><span data-stu-id="85138-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="85138-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="85138-116">Example</span></span>

<span data-ttu-id="85138-117">ICE76 segnala l'errore seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="85138-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="85138-118">[Tabella FileSFPCatalog](filesfpcatalog-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="85138-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="85138-119">file\_</span><span class="sxs-lookup"><span data-stu-id="85138-119">File\_</span></span> | <span data-ttu-id="85138-120">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="85138-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="85138-121">File1</span><span class="sxs-lookup"><span data-stu-id="85138-121">File1</span></span>  | <span data-ttu-id="85138-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="85138-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="85138-123">[Tabella azione BindImage sul](bindimage-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="85138-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="85138-124">file\_</span><span class="sxs-lookup"><span data-stu-id="85138-124">File\_</span></span> |
|--------|
| <span data-ttu-id="85138-125">File1</span><span class="sxs-lookup"><span data-stu-id="85138-125">File1</span></span>  |



 

<span data-ttu-id="85138-126">Per risolvere questo problema, non immettere file che fanno riferimento a cataloghi SFP nella tabella azione BindImage sul.</span><span class="sxs-lookup"><span data-stu-id="85138-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85138-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85138-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85138-128">Tabella azione BindImage sul</span><span class="sxs-lookup"><span data-stu-id="85138-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="85138-129">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="85138-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="85138-130">Tabella FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="85138-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="85138-131">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="85138-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



