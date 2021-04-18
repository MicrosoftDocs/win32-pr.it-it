---
description: La tabella FileSFPCatalog associa i file specificati ai file di catalogo utilizzati dalla protezione dei file di sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabella FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315470"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="3286e-103">Tabella FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="3286e-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="3286e-104">La tabella FileSFPCatalog associa i file specificati ai file di catalogo utilizzati dalla protezione dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="3286e-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="3286e-105">**Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="3286e-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="3286e-106">La tabella FileSFPCatalog include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3286e-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="3286e-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="3286e-107">Column</span></span>       | <span data-ttu-id="3286e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3286e-108">Type</span></span>                         | <span data-ttu-id="3286e-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="3286e-109">Key</span></span> | <span data-ttu-id="3286e-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="3286e-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="3286e-111">file\_</span><span class="sxs-lookup"><span data-stu-id="3286e-111">File\_</span></span>       | [<span data-ttu-id="3286e-112">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3286e-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="3286e-113">S</span><span class="sxs-lookup"><span data-stu-id="3286e-113">Y</span></span>   | <span data-ttu-id="3286e-114">N</span><span class="sxs-lookup"><span data-stu-id="3286e-114">N</span></span>        |
| <span data-ttu-id="3286e-115">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="3286e-115">SFPCatalog\_</span></span> | [<span data-ttu-id="3286e-116">Filename</span><span class="sxs-lookup"><span data-stu-id="3286e-116">Filename</span></span>](filename.md)     | <span data-ttu-id="3286e-117">S</span><span class="sxs-lookup"><span data-stu-id="3286e-117">Y</span></span>   | <span data-ttu-id="3286e-118">N</span><span class="sxs-lookup"><span data-stu-id="3286e-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3286e-119">Colonne</span><span class="sxs-lookup"><span data-stu-id="3286e-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3286e-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="3286e-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="3286e-121">Chiave esterna per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3286e-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="3286e-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="3286e-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="3286e-123">Chiave esterna per la [tabella SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3286e-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3286e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3286e-124">Remarks</span></span>

<span data-ttu-id="3286e-125">L' [azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella FileSFPCatalog e sulla [tabella SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3286e-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="3286e-126">Convalida</span><span class="sxs-lookup"><span data-stu-id="3286e-126">Validation</span></span>

<dl>

[<span data-ttu-id="3286e-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="3286e-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3286e-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="3286e-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3286e-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="3286e-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3286e-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="3286e-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="3286e-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="3286e-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



