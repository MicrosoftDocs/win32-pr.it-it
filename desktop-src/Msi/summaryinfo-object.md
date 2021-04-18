---
description: L'oggetto SummaryInfo viene usato per leggere, creare e aggiornare le proprietà del documento dal flusso di informazioni di riepilogo di un oggetto di archiviazione.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Oggetto SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329244"
---
# <a name="summaryinfo-object"></a><span data-ttu-id="e3b77-103">Oggetto SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="e3b77-103">SummaryInfo object</span></span>

<span data-ttu-id="e3b77-104">L'oggetto **SummaryInfo** viene usato per leggere, creare e aggiornare le proprietà del documento dal [flusso di informazioni di riepilogo](summary-information-stream.md) di un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3b77-104">The **SummaryInfo** object is used to read, create, and update document properties from the [summary information stream](summary-information-stream.md) of a storage object.</span></span>

## <a name="members"></a><span data-ttu-id="e3b77-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e3b77-105">Members</span></span>

<span data-ttu-id="e3b77-106">L'oggetto **SummaryInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3b77-106">The **SummaryInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="e3b77-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="e3b77-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="e3b77-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3b77-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e3b77-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e3b77-109">Methods</span></span>

<span data-ttu-id="e3b77-110">L'oggetto **SummaryInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e3b77-110">The **SummaryInfo** object has these methods.</span></span>



| <span data-ttu-id="e3b77-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="e3b77-111">Method</span></span>                                 | <span data-ttu-id="e3b77-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3b77-112">Description</span></span>                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b77-113">**Rendere persistenti**</span><span class="sxs-lookup"><span data-stu-id="e3b77-113">**Persist**</span></span>](summaryinfo-persist.md) | <span data-ttu-id="e3b77-114">Formatta e scrive le proprietà archiviate in precedenza nel [flusso di informazioni di riepilogo](summary-information-stream.md)standard.</span><span class="sxs-lookup"><span data-stu-id="e3b77-114">Formats and writes the previously stored properties into the standard [summary information stream](summary-information-stream.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e3b77-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3b77-115">Properties</span></span>

<span data-ttu-id="e3b77-116">L'oggetto **SummaryInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3b77-116">The **SummaryInfo** object has these properties.</span></span>



| <span data-ttu-id="e3b77-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3b77-117">Property</span></span>                                                                             | <span data-ttu-id="e3b77-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3b77-118">Description</span></span>                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b77-119">**Proprietà Property (oggetto SummaryInfo)**</span><span class="sxs-lookup"><span data-stu-id="e3b77-119">**Property Property (SummaryInfo Object)**</span></span>](summaryinfo-summaryinfo.md)<br/> | <span data-ttu-id="e3b77-120">Ottiene o imposta il valore per la proprietà specificata nel flusso di informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e3b77-120">Gets or sets the value for the specified property in the summary information stream.</span></span><br/> |
| [<span data-ttu-id="e3b77-121">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="e3b77-121">**PropertyCount**</span></span>](summaryinfo-propertycount.md)<br/>                        | <span data-ttu-id="e3b77-122">Indica il numero corrente di valori di proprietà nell'oggetto informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e3b77-122">Indicates the current number of property values in the summary information object.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="e3b77-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3b77-123">Requirements</span></span>



| <span data-ttu-id="e3b77-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b77-124">Requirement</span></span> | <span data-ttu-id="e3b77-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b77-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b77-126">Versione</span><span class="sxs-lookup"><span data-stu-id="e3b77-126">Version</span></span><br/> | <span data-ttu-id="e3b77-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e3b77-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e3b77-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3b77-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e3b77-129">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3b77-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e3b77-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b77-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3b77-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b77-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e3b77-132">IID</span><span class="sxs-lookup"><span data-stu-id="e3b77-132">IID</span></span><br/>     | <span data-ttu-id="e3b77-133">IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e3b77-133">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="e3b77-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3b77-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b77-135">**Proprietà SummaryInformation (oggetto di database)**</span><span class="sxs-lookup"><span data-stu-id="e3b77-135">**SummaryInformation Property (Database Object)**</span></span>](database-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="e3b77-136">**Proprietà SummaryInformation (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="e3b77-136">**SummaryInformation Property (Installer Object)**</span></span>](installer-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="e3b77-137">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e3b77-137">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




