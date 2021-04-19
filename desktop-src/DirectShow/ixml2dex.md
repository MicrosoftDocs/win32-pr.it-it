---
description: L'interfaccia IXml2Dex Salva e carica i file di progetto di servizi di modifica DirectShow (DES) in Extensible Markup Language (XML). Questa interfaccia fornisce anche metodi per la lettura e la scrittura di file di grafico DirectShow (con estensione GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaccia IXml2Dex (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332564"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="a5531-104">Interfaccia IXml2Dex</span><span class="sxs-lookup"><span data-stu-id="a5531-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="a5531-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a5531-105">\[Deprecated.</span></span> <span data-ttu-id="a5531-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5531-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a5531-107">L' `IXml2Dex` interfaccia Salva e carica i file di progetto di [servizi di modifica DirectShow](directshow-editing-services.md) (DES) in Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="a5531-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="a5531-108">Questa interfaccia fornisce anche metodi per la lettura e la scrittura di file di grafico DirectShow (con estensione GRF).</span><span class="sxs-lookup"><span data-stu-id="a5531-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="a5531-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a5531-109">Members</span></span>

<span data-ttu-id="a5531-110">L'interfaccia **IXml2Dex** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a5531-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a5531-111">**IXml2Dex** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5531-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="a5531-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5531-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a5531-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5531-113">Methods</span></span>

<span data-ttu-id="a5531-114">L'interfaccia **IXml2Dex** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a5531-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="a5531-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a5531-115">Method</span></span>                                                      | <span data-ttu-id="a5531-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5531-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="a5531-117">**CopyXML**</span><span class="sxs-lookup"><span data-stu-id="a5531-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="a5531-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-119">**CreateGraphFromFile**</span><span class="sxs-lookup"><span data-stu-id="a5531-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="a5531-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-121">**Delete**</span><span class="sxs-lookup"><span data-stu-id="a5531-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="a5531-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-123">**PasteXML**</span><span class="sxs-lookup"><span data-stu-id="a5531-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="a5531-124">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-125">**PasteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="a5531-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="a5531-126">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-127">**ReadXML**</span><span class="sxs-lookup"><span data-stu-id="a5531-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="a5531-128">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-129">**ReadXMLFile**</span><span class="sxs-lookup"><span data-stu-id="a5531-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="a5531-130">Carica un file di progetto XML.</span><span class="sxs-lookup"><span data-stu-id="a5531-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="a5531-131">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a5531-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="a5531-132">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="a5531-133">**WriteGrfFile**</span><span class="sxs-lookup"><span data-stu-id="a5531-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="a5531-134">Scrive un grafico di filtro in un file in formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="a5531-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="a5531-135">**WriteXML**</span><span class="sxs-lookup"><span data-stu-id="a5531-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="a5531-136">Converte una sequenza temporale in una stringa XML.</span><span class="sxs-lookup"><span data-stu-id="a5531-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="a5531-137">**WriteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="a5531-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="a5531-138">Converte una sequenza temporale in XML e scrive i dati XML in un file.</span><span class="sxs-lookup"><span data-stu-id="a5531-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="a5531-139">**WriteXMLPart**</span><span class="sxs-lookup"><span data-stu-id="a5531-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="a5531-140">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="a5531-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="a5531-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5531-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5531-142">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a5531-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a5531-143">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a5531-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a5531-144">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a5531-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5531-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5531-145">Requirements</span></span>



| <span data-ttu-id="a5531-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5531-146">Requirement</span></span> | <span data-ttu-id="a5531-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a5531-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5531-148">Versione</span><span class="sxs-lookup"><span data-stu-id="a5531-148">Version</span></span><br/> | <span data-ttu-id="a5531-149">Internet Explorer 4,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a5531-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="a5531-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5531-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a5531-151"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a5531-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5531-152">Library</span></span><br/> | <dl> <span data-ttu-id="a5531-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
