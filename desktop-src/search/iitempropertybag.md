---
description: Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca. Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interfaccia IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128503"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="a99d5-104">Interfaccia IItemPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a99d5-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="a99d5-105">Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a99d5-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="a99d5-106">Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a99d5-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="a99d5-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a99d5-107">Members</span></span>

<span data-ttu-id="a99d5-108">L'interfaccia **IItemPropertyBag** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a99d5-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a99d5-109">**IItemPropertyBag** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a99d5-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="a99d5-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a99d5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a99d5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a99d5-111">Methods</span></span>

<span data-ttu-id="a99d5-112">L'interfaccia **IItemPropertyBag** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a99d5-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="a99d5-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a99d5-113">Method</span></span>                                                      | <span data-ttu-id="a99d5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a99d5-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a99d5-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a99d5-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="a99d5-116">Ottiene un conteggio del numero di proprietà nell'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a99d5-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="a99d5-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a99d5-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="a99d5-118">Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a99d5-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="a99d5-119">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="a99d5-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="a99d5-120">Determina la lettura di una o più proprietà dall'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a99d5-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="a99d5-121">**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="a99d5-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="a99d5-122">Determina il salvataggio di una o più proprietà nel contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a99d5-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a99d5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a99d5-123">Remarks</span></span>

<span data-ttu-id="a99d5-124">L'interfaccia **IItemPropertyBag** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a99d5-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a99d5-125">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **IItemPropertyBag** e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="a99d5-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99d5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a99d5-126">Requirements</span></span>



| <span data-ttu-id="a99d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99d5-127">Requirement</span></span> | <span data-ttu-id="a99d5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a99d5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a99d5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a99d5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a99d5-130">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a99d5-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a99d5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a99d5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a99d5-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a99d5-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a99d5-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a99d5-133">Redistributable</span></span><br/>          | <span data-ttu-id="a99d5-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a99d5-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
