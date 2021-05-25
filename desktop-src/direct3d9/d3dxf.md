---
description: Opzioni di formato di file X, caricamento e salvataggio.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343646"
---
# <a name="d3dxf"></a><span data-ttu-id="720d2-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="720d2-103">D3DXF</span></span>

<span data-ttu-id="720d2-104">Opzioni di formato di file X, caricamento e salvataggio.</span><span class="sxs-lookup"><span data-stu-id="720d2-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="720d2-105">Formati di file</span><span class="sxs-lookup"><span data-stu-id="720d2-105">File Formats</span></span>

<span data-ttu-id="720d2-106">Nella tabella seguente viene specificato il tipo di dati del file:</span><span class="sxs-lookup"><span data-stu-id="720d2-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="720d2-107">\#definisce per formato di file</span><span class="sxs-lookup"><span data-stu-id="720d2-107">\#defines for File Format</span></span>     | <span data-ttu-id="720d2-108">Valore</span><span class="sxs-lookup"><span data-stu-id="720d2-108">Value</span></span> | <span data-ttu-id="720d2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720d2-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="720d2-110">D3DXF \_ FILEFORMAT \_ BINARY</span><span class="sxs-lookup"><span data-stu-id="720d2-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="720d2-111">0</span><span class="sxs-lookup"><span data-stu-id="720d2-111">0</span></span>     | <span data-ttu-id="720d2-112">File binario in formato legacy.</span><span class="sxs-lookup"><span data-stu-id="720d2-112">Legacy-format binary file.</span></span> <span data-ttu-id="720d2-113">Vedere [X File Reference (Legacy) (Informazioni di riferimento sul file X (legacy)](dx9-graphics-reference-x-file.md)).</span><span class="sxs-lookup"><span data-stu-id="720d2-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="720d2-114">D3DXF \_ FILEFORMAT \_ TEXT</span><span class="sxs-lookup"><span data-stu-id="720d2-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="720d2-115">1</span><span class="sxs-lookup"><span data-stu-id="720d2-115">1</span></span>     | <span data-ttu-id="720d2-116">File di testo.</span><span class="sxs-lookup"><span data-stu-id="720d2-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="720d2-117">FILEFORMAT D3DXF \_ \_ COMPRESSO</span><span class="sxs-lookup"><span data-stu-id="720d2-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="720d2-118">2</span><span class="sxs-lookup"><span data-stu-id="720d2-118">2</span></span>     | <span data-ttu-id="720d2-119">File compresso.</span><span class="sxs-lookup"><span data-stu-id="720d2-119">Compressed file.</span></span> <span data-ttu-id="720d2-120">Con questo flag è necessario specificare anche il formato binario o il formato di testo.</span><span class="sxs-lookup"><span data-stu-id="720d2-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="720d2-121">Opzioni di caricamento file</span><span class="sxs-lookup"><span data-stu-id="720d2-121">File Load Options</span></span>

<span data-ttu-id="720d2-122">La tabella seguente specifica le opzioni di caricamento dei file con file con estensione x:</span><span class="sxs-lookup"><span data-stu-id="720d2-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="720d2-123">\#Definire</span><span class="sxs-lookup"><span data-stu-id="720d2-123">\#define</span></span>                      | <span data-ttu-id="720d2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="720d2-124">Value</span></span> | <span data-ttu-id="720d2-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720d2-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="720d2-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="720d2-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="720d2-127">0</span><span class="sxs-lookup"><span data-stu-id="720d2-127">0</span></span>     | <span data-ttu-id="720d2-128">Caricare i dati da un file.</span><span class="sxs-lookup"><span data-stu-id="720d2-128">Load data from a file.</span></span>     |
| <span data-ttu-id="720d2-129">FILE D3DXFCARICA \_ \_ DAWFILE</span><span class="sxs-lookup"><span data-stu-id="720d2-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="720d2-130">1</span><span class="sxs-lookup"><span data-stu-id="720d2-130">1</span></span>     | <span data-ttu-id="720d2-131">Caricare i dati da un file.</span><span class="sxs-lookup"><span data-stu-id="720d2-131">Load data from a file.</span></span>     |
| <span data-ttu-id="720d2-132">FILELOAD D3DXF \_ \_ DARESOURCE</span><span class="sxs-lookup"><span data-stu-id="720d2-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="720d2-133">2</span><span class="sxs-lookup"><span data-stu-id="720d2-133">2</span></span>     | <span data-ttu-id="720d2-134">Caricare i dati da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="720d2-134">Load data from a resource.</span></span> |
| <span data-ttu-id="720d2-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="720d2-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="720d2-136">3</span><span class="sxs-lookup"><span data-stu-id="720d2-136">3</span></span>     | <span data-ttu-id="720d2-137">Caricare i dati dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="720d2-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="720d2-138">Opzioni di salvataggio file</span><span class="sxs-lookup"><span data-stu-id="720d2-138">File Save Options</span></span>

<span data-ttu-id="720d2-139">La tabella seguente specifica le opzioni di salvataggio e caricamento dei file con i file con estensione x:</span><span class="sxs-lookup"><span data-stu-id="720d2-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="720d2-140">\#Definire</span><span class="sxs-lookup"><span data-stu-id="720d2-140">\#define</span></span>                 | <span data-ttu-id="720d2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="720d2-141">Value</span></span> | <span data-ttu-id="720d2-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720d2-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="720d2-143">FILE D3DXFSALVA \_ \_ NEL FILE</span><span class="sxs-lookup"><span data-stu-id="720d2-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="720d2-144">0</span><span class="sxs-lookup"><span data-stu-id="720d2-144">0</span></span>     | <span data-ttu-id="720d2-145">Salvare in un file.</span><span class="sxs-lookup"><span data-stu-id="720d2-145">Save to a file.</span></span>                |
| <span data-ttu-id="720d2-146">FILE D3DXFSALVA \_ \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="720d2-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="720d2-147">1</span><span class="sxs-lookup"><span data-stu-id="720d2-147">1</span></span>     | <span data-ttu-id="720d2-148">Salvare in un file di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="720d2-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="720d2-149">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="720d2-149">Constant Information</span></span>



| <span data-ttu-id="720d2-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="720d2-150">Requirement</span></span>                         | <span data-ttu-id="720d2-151">Valore</span><span class="sxs-lookup"><span data-stu-id="720d2-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="720d2-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="720d2-152">Header</span></span>                   | <span data-ttu-id="720d2-153">d3dx9xof.h</span><span class="sxs-lookup"><span data-stu-id="720d2-153">d3dx9xof.h</span></span> |
| <span data-ttu-id="720d2-154">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="720d2-154">Minimum operating system</span></span> | <span data-ttu-id="720d2-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="720d2-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="720d2-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="720d2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="720d2-157">Costanti del file D3DX X</span><span class="sxs-lookup"><span data-stu-id="720d2-157">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="720d2-158">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="720d2-158">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



