---
description: Fornisce metodi che definiscono l'interazione tra un'interfaccia utente (UI) e gli oggetti dello spazio dei nomi di ricerca creati dall'indicizzatore.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interfaccia ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401630"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="8033f-103">Interfaccia ISearchItem</span><span class="sxs-lookup"><span data-stu-id="8033f-103">ISearchItem interface</span></span>

<span data-ttu-id="8033f-104">Fornisce metodi che definiscono l'interazione tra un'interfaccia utente (UI) e gli oggetti dello spazio dei nomi di ricerca creati dall'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="8033f-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="8033f-105">Membri</span><span class="sxs-lookup"><span data-stu-id="8033f-105">Members</span></span>

<span data-ttu-id="8033f-106">L'interfaccia **ISearchItem** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8033f-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8033f-107">**ISearchItem** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8033f-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="8033f-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="8033f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8033f-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="8033f-109">Methods</span></span>

<span data-ttu-id="8033f-110">L'interfaccia **ISearchItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8033f-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="8033f-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="8033f-111">Method</span></span>                                                         | <span data-ttu-id="8033f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8033f-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8033f-113">**GetParentFolder**</span><span class="sxs-lookup"><span data-stu-id="8033f-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="8033f-114">Ottiene l'oggetto **ISearchItem** se l'URL rappresenta un'origine dati della shell effettiva, nota anche come estensione dello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="8033f-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="8033f-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8033f-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="8033f-116">Ottiene l'oggetto dell'interfaccia utente di **ISearchItem**.</span><span class="sxs-lookup"><span data-stu-id="8033f-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="8033f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8033f-117">Remarks</span></span>

<span data-ttu-id="8033f-118">[**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) è supportato solo in Windows XP e windows Server 2003 e non deve più essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8033f-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="8033f-119">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchItem** e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="8033f-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8033f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8033f-120">Requirements</span></span>



| <span data-ttu-id="8033f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8033f-121">Requirement</span></span> | <span data-ttu-id="8033f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8033f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8033f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8033f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8033f-124">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8033f-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8033f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8033f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8033f-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8033f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8033f-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8033f-127">Redistributable</span></span><br/>          | <span data-ttu-id="8033f-128">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="8033f-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
