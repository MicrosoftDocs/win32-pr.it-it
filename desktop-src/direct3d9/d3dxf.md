---
description: X formato file, caricamento e opzioni di salvataggio.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303690"
---
# <a name="d3dxf"></a><span data-ttu-id="8a1e2-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="8a1e2-103">D3DXF</span></span>

<span data-ttu-id="8a1e2-104">X formato file, caricamento e opzioni di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="8a1e2-105">Formati di file</span><span class="sxs-lookup"><span data-stu-id="8a1e2-105">File Formats</span></span>

<span data-ttu-id="8a1e2-106">Nella tabella seguente viene specificato il tipo di dati del file:</span><span class="sxs-lookup"><span data-stu-id="8a1e2-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="8a1e2-107">\#definisce per il formato di file</span><span class="sxs-lookup"><span data-stu-id="8a1e2-107">\#defines for File Format</span></span>     | <span data-ttu-id="8a1e2-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1e2-108">Value</span></span> | <span data-ttu-id="8a1e2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a1e2-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1e2-110">\_Binario FILEFORMAT \_ D3DXF</span><span class="sxs-lookup"><span data-stu-id="8a1e2-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="8a1e2-111">0</span><span class="sxs-lookup"><span data-stu-id="8a1e2-111">0</span></span>     | <span data-ttu-id="8a1e2-112">File binario in formato legacy.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-112">Legacy-format binary file.</span></span> <span data-ttu-id="8a1e2-113">Vedere il [riferimento al file X (legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="8a1e2-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="8a1e2-114">\_Testo FILEformat D3DXF \_</span><span class="sxs-lookup"><span data-stu-id="8a1e2-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="8a1e2-115">1</span><span class="sxs-lookup"><span data-stu-id="8a1e2-115">1</span></span>     | <span data-ttu-id="8a1e2-116">File di testo.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="8a1e2-117">D3DXF \_ FileFormat \_ compresso</span><span class="sxs-lookup"><span data-stu-id="8a1e2-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="8a1e2-118">2</span><span class="sxs-lookup"><span data-stu-id="8a1e2-118">2</span></span>     | <span data-ttu-id="8a1e2-119">File compresso.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-119">Compressed file.</span></span> <span data-ttu-id="8a1e2-120">Con questo flag, è necessario specificare anche il formato binario o il formato di testo.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="8a1e2-121">Opzioni di caricamento file</span><span class="sxs-lookup"><span data-stu-id="8a1e2-121">File Load Options</span></span>

<span data-ttu-id="8a1e2-122">Nella tabella seguente vengono specificate le opzioni di caricamento file con i file con estensione x:</span><span class="sxs-lookup"><span data-stu-id="8a1e2-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="8a1e2-123">\#definire</span><span class="sxs-lookup"><span data-stu-id="8a1e2-123">\#define</span></span>                      | <span data-ttu-id="8a1e2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1e2-124">Value</span></span> | <span data-ttu-id="8a1e2-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a1e2-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="8a1e2-126">D3DXF \_ fileload \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="8a1e2-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="8a1e2-127">0</span><span class="sxs-lookup"><span data-stu-id="8a1e2-127">0</span></span>     | <span data-ttu-id="8a1e2-128">Caricare i dati da un file.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-128">Load data from a file.</span></span>     |
| <span data-ttu-id="8a1e2-129">D3DXF \_ fileload \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="8a1e2-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="8a1e2-130">1</span><span class="sxs-lookup"><span data-stu-id="8a1e2-130">1</span></span>     | <span data-ttu-id="8a1e2-131">Caricare i dati da un file.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-131">Load data from a file.</span></span>     |
| <span data-ttu-id="8a1e2-132">D3DXF \_ fileload \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="8a1e2-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="8a1e2-133">2</span><span class="sxs-lookup"><span data-stu-id="8a1e2-133">2</span></span>     | <span data-ttu-id="8a1e2-134">Caricare i dati da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-134">Load data from a resource.</span></span> |
| <span data-ttu-id="8a1e2-135">D3DXF \_ fileload \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="8a1e2-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="8a1e2-136">3</span><span class="sxs-lookup"><span data-stu-id="8a1e2-136">3</span></span>     | <span data-ttu-id="8a1e2-137">Caricare i dati dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="8a1e2-138">Opzioni di salvataggio file</span><span class="sxs-lookup"><span data-stu-id="8a1e2-138">File Save Options</span></span>

<span data-ttu-id="8a1e2-139">La tabella seguente specifica le opzioni di salvataggio e caricamento dei file con i file con estensione x:</span><span class="sxs-lookup"><span data-stu-id="8a1e2-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="8a1e2-140">\#definire</span><span class="sxs-lookup"><span data-stu-id="8a1e2-140">\#define</span></span>                 | <span data-ttu-id="8a1e2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1e2-141">Value</span></span> | <span data-ttu-id="8a1e2-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a1e2-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="8a1e2-143">\_File D3DXF FILEsave \_</span><span class="sxs-lookup"><span data-stu-id="8a1e2-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="8a1e2-144">0</span><span class="sxs-lookup"><span data-stu-id="8a1e2-144">0</span></span>     | <span data-ttu-id="8a1e2-145">Salva in un file.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-145">Save to a file.</span></span>                |
| <span data-ttu-id="8a1e2-146">D3DXF \_ FileSave \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="8a1e2-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="8a1e2-147">1</span><span class="sxs-lookup"><span data-stu-id="8a1e2-147">1</span></span>     | <span data-ttu-id="8a1e2-148">Salva in un file a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="8a1e2-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="8a1e2-149">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="8a1e2-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="8a1e2-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a1e2-150">Header</span></span>                   | <span data-ttu-id="8a1e2-151">d3dx9xof. h</span><span class="sxs-lookup"><span data-stu-id="8a1e2-151">d3dx9xof.h</span></span> |
| <span data-ttu-id="8a1e2-152">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="8a1e2-152">Minimum operating system</span></span> | <span data-ttu-id="8a1e2-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8a1e2-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8a1e2-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a1e2-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a1e2-155">Costanti file D3DX X</span><span class="sxs-lookup"><span data-stu-id="8a1e2-155">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="8a1e2-156">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="8a1e2-156">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



