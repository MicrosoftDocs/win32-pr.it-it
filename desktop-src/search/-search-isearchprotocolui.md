---
description: Fornisce un metodo per richiamare gli oggetti ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interfaccia ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306159"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="b36e3-103">Interfaccia ISearchProtocolUI</span><span class="sxs-lookup"><span data-stu-id="b36e3-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="b36e3-104">Fornisce un metodo per richiamare gli oggetti [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b36e3-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="b36e3-105">I metodi in questa interfaccia vengono chiamati dall'host del protocollo durante l'elaborazione degli URL dal gatherer.</span><span class="sxs-lookup"><span data-stu-id="b36e3-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="b36e3-106">Il gestore di protocollo implementa il protocollo per l'accesso a un'origine di contenuto nel formato nativo e questa interfaccia implementa un gestore di protocollo personalizzato per espandere le origini dati che possono essere indicizzate.</span><span class="sxs-lookup"><span data-stu-id="b36e3-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="b36e3-107">Membri</span><span class="sxs-lookup"><span data-stu-id="b36e3-107">Members</span></span>

<span data-ttu-id="b36e3-108">L'interfaccia **ISearchProtocolUI** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b36e3-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b36e3-109">**ISearchProtocolUI** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b36e3-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="b36e3-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b36e3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b36e3-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b36e3-111">Methods</span></span>

<span data-ttu-id="b36e3-112">L'interfaccia **ISearchProtocolUI** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b36e3-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="b36e3-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="b36e3-113">Method</span></span>                                                                       | <span data-ttu-id="b36e3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b36e3-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36e3-115">**GetSearchItemForUrl**</span><span class="sxs-lookup"><span data-stu-id="b36e3-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="b36e3-116">Ottiene l'elemento di ricerca per i dati specificati.</span><span class="sxs-lookup"><span data-stu-id="b36e3-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="b36e3-117">Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b36e3-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b36e3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b36e3-118">Remarks</span></span>

<span data-ttu-id="b36e3-119">L'interfaccia **ISearchProtocolUI** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b36e3-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b36e3-120">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchProtocolUI** e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="b36e3-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36e3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b36e3-121">Requirements</span></span>



| <span data-ttu-id="b36e3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b36e3-122">Requirement</span></span> | <span data-ttu-id="b36e3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b36e3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b36e3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b36e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b36e3-125">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b36e3-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b36e3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b36e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b36e3-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b36e3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b36e3-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b36e3-128">Redistributable</span></span><br/>          | <span data-ttu-id="b36e3-129">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b36e3-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
