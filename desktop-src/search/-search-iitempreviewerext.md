---
description: Fornisce metodi per fornire le impostazioni del browser. L'interfaccia IItemPreviewerExt è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interfaccia IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966534"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="6bb62-104">Interfaccia IItemPreviewerExt</span><span class="sxs-lookup"><span data-stu-id="6bb62-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="6bb62-105">Fornisce metodi per fornire le impostazioni del browser.</span><span class="sxs-lookup"><span data-stu-id="6bb62-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="6bb62-106">L'interfaccia **IItemPreviewerExt** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6bb62-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="6bb62-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6bb62-107">Members</span></span>

<span data-ttu-id="6bb62-108">L'interfaccia **IItemPreviewerExt** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6bb62-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6bb62-109">**IItemPreviewerExt** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6bb62-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="6bb62-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6bb62-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6bb62-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6bb62-111">Methods</span></span>

<span data-ttu-id="6bb62-112">L'interfaccia **IItemPreviewerExt** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6bb62-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="6bb62-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="6bb62-113">Method</span></span>                                                                               | <span data-ttu-id="6bb62-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bb62-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bb62-115">**GetLinkedContent**</span><span class="sxs-lookup"><span data-stu-id="6bb62-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="6bb62-116">Consente all'estensione di contenuti avanzati per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="6bb62-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="6bb62-117">**GetRelatedPart**</span><span class="sxs-lookup"><span data-stu-id="6bb62-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="6bb62-118">Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.</span><span class="sxs-lookup"><span data-stu-id="6bb62-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="6bb62-119">**ProcessTransformCommand**</span><span class="sxs-lookup"><span data-stu-id="6bb62-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="6bb62-120">Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.</span><span class="sxs-lookup"><span data-stu-id="6bb62-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="6bb62-121">**SuggestBrowserPolicy**</span><span class="sxs-lookup"><span data-stu-id="6bb62-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="6bb62-122">Suggerisce che i criteri di sicurezza devono essere applicati al browser.</span><span class="sxs-lookup"><span data-stu-id="6bb62-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="6bb62-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bb62-123">Remarks</span></span>

<span data-ttu-id="6bb62-124">L'interfaccia **IItemPreviewerExt** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6bb62-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="6bb62-125">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **IItemPreviewerExt** e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb62-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb62-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bb62-126">Requirements</span></span>



| <span data-ttu-id="6bb62-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb62-127">Requirement</span></span> | <span data-ttu-id="6bb62-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6bb62-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bb62-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bb62-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb62-130">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bb62-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6bb62-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bb62-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb62-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6bb62-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6bb62-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6bb62-133">Redistributable</span></span><br/>          | <span data-ttu-id="6bb62-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="6bb62-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
