---
description: La tabella SFPCatalog contiene i cataloghi usati da Windows me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabella SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226352"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="8e979-103">Tabella SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="8e979-103">SFPCatalog Table</span></span>

<span data-ttu-id="8e979-104">La tabella SFPCatalog contiene i cataloghi usati da Windows me.</span><span class="sxs-lookup"><span data-stu-id="8e979-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="8e979-105">La tabella SFPCatalog include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e979-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="8e979-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="8e979-106">Column</span></span>     | <span data-ttu-id="8e979-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e979-107">Type</span></span>                       | <span data-ttu-id="8e979-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="8e979-108">Key</span></span> | <span data-ttu-id="8e979-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e979-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="8e979-110">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="8e979-110">SFPCatalog</span></span> | [<span data-ttu-id="8e979-111">Filename</span><span class="sxs-lookup"><span data-stu-id="8e979-111">Filename</span></span>](filename.md)   | <span data-ttu-id="8e979-112">S</span><span class="sxs-lookup"><span data-stu-id="8e979-112">Y</span></span>   | <span data-ttu-id="8e979-113">N</span><span class="sxs-lookup"><span data-stu-id="8e979-113">N</span></span>        |
| <span data-ttu-id="8e979-114">Catalogo</span><span class="sxs-lookup"><span data-stu-id="8e979-114">Catalog</span></span>    | [<span data-ttu-id="8e979-115">Binario</span><span class="sxs-lookup"><span data-stu-id="8e979-115">Binary</span></span>](binary.md)       | <span data-ttu-id="8e979-116">N</span><span class="sxs-lookup"><span data-stu-id="8e979-116">N</span></span>   | <span data-ttu-id="8e979-117">N</span><span class="sxs-lookup"><span data-stu-id="8e979-117">N</span></span>        |
| <span data-ttu-id="8e979-118">Dipendenza</span><span class="sxs-lookup"><span data-stu-id="8e979-118">Dependency</span></span> | [<span data-ttu-id="8e979-119">Formattato</span><span class="sxs-lookup"><span data-stu-id="8e979-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="8e979-120">N</span><span class="sxs-lookup"><span data-stu-id="8e979-120">N</span></span>   | <span data-ttu-id="8e979-121">S</span><span class="sxs-lookup"><span data-stu-id="8e979-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8e979-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="8e979-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8e979-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="8e979-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="8e979-124">Nome di file breve per il catalogo.</span><span class="sxs-lookup"><span data-stu-id="8e979-124">The short file name for the catalog.</span></span> <span data-ttu-id="8e979-125">Poiché i cataloghi non hanno versione, il catalogo specificato in questa colonna può sovrascrivere un catalogo con lo stesso nome ed è già installato nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="8e979-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="8e979-126">Vedere l'argomento relativo al controllo delle versioni dei file. [Nessun file ha una versione](neither-file-has-a-version.md).</span><span class="sxs-lookup"><span data-stu-id="8e979-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e979-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo</span><span class="sxs-lookup"><span data-stu-id="8e979-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="8e979-128">Dati binari per il catalogo.</span><span class="sxs-lookup"><span data-stu-id="8e979-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="8e979-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dipendenza</span><span class="sxs-lookup"><span data-stu-id="8e979-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="8e979-130">Il catalogo specificato in questo campo è l'elemento padre del catalogo dipendente specificato nel campo SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="8e979-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="8e979-131">Immettere il nome file breve del catalogo padre nel campo dipendenza.</span><span class="sxs-lookup"><span data-stu-id="8e979-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="8e979-132">Questo campo è una chiave di nuovo nella colonna SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="8e979-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="8e979-133">La corrispondenza tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8e979-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="8e979-134">Se il campo di dipendenza fa riferimento a un altro record nella tabella SFPCatalog, il catalogo padre viene installato prima del catalogo dipendente.</span><span class="sxs-lookup"><span data-stu-id="8e979-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="8e979-135">Se il campo di dipendenza fa riferimento a un catalogo padre non presente nel campo SFPCatalog della tabella e se il catalogo padre non è già installato, l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="8e979-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e979-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e979-136">Remarks</span></span>

<span data-ttu-id="8e979-137">L' [azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella [FileSFPCatalog](filesfpcatalog-table.md) e sulla tabella SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="8e979-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="8e979-138">Convalida</span><span class="sxs-lookup"><span data-stu-id="8e979-138">Validation</span></span>

<dl>

[<span data-ttu-id="8e979-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="8e979-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8e979-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="8e979-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8e979-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="8e979-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="8e979-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="8e979-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8e979-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="8e979-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8e979-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="8e979-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



