---
description: L'interfaccia IMediaLocator fornisce metodi per la convalida dei nomi di file nei servizi di modifica DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interfaccia IMediaLocator (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325032"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="58aee-103">Interfaccia IMediaLocator</span><span class="sxs-lookup"><span data-stu-id="58aee-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="58aee-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="58aee-104">\[Deprecated.</span></span> <span data-ttu-id="58aee-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58aee-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58aee-106">L' `IMediaLocator` interfaccia fornisce metodi per la convalida dei nomi di file in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="58aee-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="58aee-107">Usare questa interfaccia per assicurarsi che un nome file e un percorso specificati corrispondano a un file esistente.</span><span class="sxs-lookup"><span data-stu-id="58aee-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="58aee-108">Questa interfaccia fornisce inoltre un modo per cercare il file in altre posizioni e per visualizzare una finestra di dialogo **aperta** in modo che l'utente possa individuare il file.</span><span class="sxs-lookup"><span data-stu-id="58aee-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="58aee-109">Il localizzatore multimediale implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="58aee-109">The media locator implements this interface.</span></span> <span data-ttu-id="58aee-110">La sequenza temporale e il motore di rendering supportano anche la convalida dei nomi di file tramite i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="58aee-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="58aee-111">[**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): convalida e aggiorna i nomi di file nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="58aee-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="58aee-112">[**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): specifica il modo in cui il motore di rendering convalida i nomi di file in fase di rendering.</span><span class="sxs-lookup"><span data-stu-id="58aee-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="58aee-113">In genere, un'applicazione DES chiamerà questi metodi anziché creare direttamente un'istanza del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="58aee-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="58aee-114">Per ulteriori informazioni, vedere [utilizzo del localizzatore multimediale](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="58aee-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="58aee-115">Membri</span><span class="sxs-lookup"><span data-stu-id="58aee-115">Members</span></span>

<span data-ttu-id="58aee-116">L'interfaccia **IMediaLocator** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="58aee-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="58aee-117">**IMediaLocator** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="58aee-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="58aee-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="58aee-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58aee-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="58aee-119">Methods</span></span>

<span data-ttu-id="58aee-120">L'interfaccia **IMediaLocator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="58aee-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="58aee-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="58aee-121">Method</span></span>                                                     | <span data-ttu-id="58aee-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58aee-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="58aee-123">**AddFoundLocation**</span><span class="sxs-lookup"><span data-stu-id="58aee-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="58aee-124">Aggiunge una directory alla cache di directory.</span><span class="sxs-lookup"><span data-stu-id="58aee-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="58aee-125">**FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="58aee-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="58aee-126">Cerca un file e, in caso di esito positivo, recupera il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="58aee-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58aee-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="58aee-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58aee-128">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="58aee-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58aee-129">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="58aee-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58aee-130">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="58aee-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58aee-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58aee-131">Requirements</span></span>



| <span data-ttu-id="58aee-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="58aee-132">Requirement</span></span> | <span data-ttu-id="58aee-133">Valore</span><span class="sxs-lookup"><span data-stu-id="58aee-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58aee-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58aee-134">Header</span></span><br/>  | <dl> <span data-ttu-id="58aee-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="58aee-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58aee-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="58aee-136">Library</span></span><br/> | <dl> <span data-ttu-id="58aee-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58aee-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
