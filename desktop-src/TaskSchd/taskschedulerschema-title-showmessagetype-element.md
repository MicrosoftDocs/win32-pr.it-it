---
title: Elemento title (showMessageType)
description: Contiene il titolo della finestra di messaggio.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Utilità di pianificazione elemento titolo
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119215"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="75402-104">Elemento title (showMessageType)</span><span class="sxs-lookup"><span data-stu-id="75402-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="75402-105">Contiene il titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="75402-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="75402-106">L'elemento **title** è definito dal tipo complesso [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75402-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="75402-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="75402-107">Parent element</span></span>



| <span data-ttu-id="75402-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="75402-108">Element</span></span>                                                                                  | <span data-ttu-id="75402-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="75402-109">Derived from</span></span>                                                               | <span data-ttu-id="75402-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75402-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="75402-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="75402-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="75402-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="75402-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="75402-113">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="75402-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="75402-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="75402-114">Remarks</span></span>

<span data-ttu-id="75402-115">Per lo sviluppo in C++, vedere [**proprietà title di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="75402-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="75402-116">Per lo sviluppo di script, vedere [**ShowMessageAction. title**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="75402-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75402-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75402-117">Requirements</span></span>



| <span data-ttu-id="75402-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75402-118">Requirement</span></span> | <span data-ttu-id="75402-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75402-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75402-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75402-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75402-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75402-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75402-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75402-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75402-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75402-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





