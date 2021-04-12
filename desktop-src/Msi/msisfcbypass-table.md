---
description: La tabella MsiSFCBypass contiene un elenco di file che devono ignorare la protezione dei file di Windows quando i file vengono installati in Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabella MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347336"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="7af43-103">Tabella MsiSFCBypass</span><span class="sxs-lookup"><span data-stu-id="7af43-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="7af43-104">La tabella MsiSFCBypass contiene un elenco di file che devono ignorare la protezione dei file di Windows quando i file vengono installati in Microsoft Windows me.</span><span class="sxs-lookup"><span data-stu-id="7af43-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="7af43-105">La tabella MsiSFCBypass include la colonna seguente.</span><span class="sxs-lookup"><span data-stu-id="7af43-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="7af43-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="7af43-106">Column</span></span> | <span data-ttu-id="7af43-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7af43-107">Type</span></span>                         | <span data-ttu-id="7af43-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="7af43-108">Key</span></span> | <span data-ttu-id="7af43-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7af43-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="7af43-110">file\_</span><span class="sxs-lookup"><span data-stu-id="7af43-110">File\_</span></span> | [<span data-ttu-id="7af43-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7af43-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="7af43-112">S</span><span class="sxs-lookup"><span data-stu-id="7af43-112">Y</span></span>   | <span data-ttu-id="7af43-113">N</span><span class="sxs-lookup"><span data-stu-id="7af43-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7af43-114">Colonne</span><span class="sxs-lookup"><span data-stu-id="7af43-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7af43-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="7af43-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="7af43-116">Chiave esterna per la [tabella file](file-table.md) che specifica il file che deve ignorare la protezione dei file di Windows quando il file viene installato in Windows me.</span><span class="sxs-lookup"><span data-stu-id="7af43-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



