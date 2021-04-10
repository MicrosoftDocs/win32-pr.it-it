---
description: L'interfaccia IWiaSegmentationFilter rileva le aree secondarie di un flusso di immagini e crea elementi IWiaItem2 separati per ognuno di essi.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaccia IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879318"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="5e556-103">Interfaccia IWiaSegmentationFilter</span><span class="sxs-lookup"><span data-stu-id="5e556-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="5e556-104">L'interfaccia **IWiaSegmentationFilter** rileva le aree secondarie di un flusso di immagini e crea elementi [**IWiaItem2**](-wia-iwiaitem2.md) separati per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="5e556-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="5e556-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5e556-105">Members</span></span>

<span data-ttu-id="5e556-106">L'interfaccia **IWiaSegmentationFilter** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e556-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5e556-107">**IWiaSegmentationFilter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e556-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="5e556-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e556-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e556-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e556-109">Methods</span></span>

<span data-ttu-id="5e556-110">L'interfaccia **IWiaSegmentationFilter** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5e556-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="5e556-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5e556-111">Method</span></span>                                                             | <span data-ttu-id="5e556-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e556-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e556-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="5e556-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="5e556-114">Determina le aree secondarie di un'immagine disposte sulla piastra piana, in modo che ogni area secondaria possa essere acquisita in un elemento immagine separato.</span><span class="sxs-lookup"><span data-stu-id="5e556-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e556-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e556-115">Remarks</span></span>

<span data-ttu-id="5e556-116">Un'applicazione deve usare [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) per creare una nuova istanza del filtro di segmentazione.</span><span class="sxs-lookup"><span data-stu-id="5e556-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="5e556-117">Un'applicazione in genere chiama questa funzione prima di visualizzarne la finestra di anteprima.</span><span class="sxs-lookup"><span data-stu-id="5e556-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="5e556-118">Quando si implementa questo filtro, utilizzare [**IWiaItem2:: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) per creare gli elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="5e556-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="5e556-119">L'applicazione deve passare **i \_ \_ \_ valori della proprietà copia padre** al parametro *ICreationFlags* per garantire che le proprietà, ad esempio il formato di immagine e la risoluzione, siano le stesse nell'elemento figlio appena creato come nell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="5e556-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="5e556-120">Un filtro di segmentazione deve supportare tutti i formati di immagine supportati dal driver.</span><span class="sxs-lookup"><span data-stu-id="5e556-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="5e556-121">Il filtro fornito da Microsoft supporta bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="5e556-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="5e556-122">Il filtro di segmentazione deve essere utilizzato solo su elementi di film e scanner di piano.</span><span class="sxs-lookup"><span data-stu-id="5e556-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="5e556-123">Per l'analisi dei film, uno scanner spesso è dotato di frame fissi, nel qual caso il driver ha creato gli elementi figlio e l'applicazione non deve richiamare il filtro di segmentazione.</span><span class="sxs-lookup"><span data-stu-id="5e556-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="5e556-124">L'interfaccia **IWiaSegmentationFilter** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e556-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="5e556-125">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e556-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="5e556-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e556-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5e556-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="5e556-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="5e556-128">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="5e556-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="5e556-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="5e556-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="5e556-130">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="5e556-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="5e556-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="5e556-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="5e556-132">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="5e556-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="5e556-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e556-133">Requirements</span></span>



| <span data-ttu-id="5e556-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e556-134">Requirement</span></span> | <span data-ttu-id="5e556-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5e556-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e556-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e556-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5e556-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e556-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e556-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e556-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5e556-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e556-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e556-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e556-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e556-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e556-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e556-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5e556-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e556-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e556-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
