---
description: Specifica la direzione di un oggetto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumerazione ContextLinkDirection (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882473"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="5ac77-103">Enumerazione ContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="5ac77-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="5ac77-104">Specifica la direzione di un oggetto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac77-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ac77-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="5ac77-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5ac77-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ac77-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**\_LinksWith ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="5ac77-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="5ac77-108">[**IContextNode**](icontextnode.md) è un disegno direzionale che punta lontano da [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="5ac77-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ac77-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**\_LinksFrom ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="5ac77-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="5ac77-110">[**IContextNode**](icontextnode.md) è un disegno direzionale che punta al [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="5ac77-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ac77-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**\_CollegamentiPer ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="5ac77-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="5ac77-112">Nessun disegno direzionale nel collegamento.</span><span class="sxs-lookup"><span data-stu-id="5ac77-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="5ac77-113">Un disegno Ink può ad esempio sottolineare una parola di input penna.</span><span class="sxs-lookup"><span data-stu-id="5ac77-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="5ac77-114">Non esiste alcuna direzione dedotta dalla sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="5ac77-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5ac77-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ac77-115">Examples</span></span>

<span data-ttu-id="5ac77-116">Nell'esempio seguente viene utilizzato un oggetto [**IContextNode**](icontextnode.md) , `m_pSelectedNode` , e vengono salvati tutti gli oggetti **IContextNode** a cui si collegano spostando l'albero predecessore e aggiungendo gli oggetti in un `CArray` oggetto `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="5ac77-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="5ac77-117">`CheckHResult` è una funzione che accetta un oggetto `HRESULT` e una stringa e genera un'eccezione creata con la stringa se `HRESULT` non ha **esito positivo**.</span><span class="sxs-lookup"><span data-stu-id="5ac77-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a><span data-ttu-id="5ac77-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac77-118">Requirements</span></span>



| <span data-ttu-id="5ac77-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac77-119">Requirement</span></span> | <span data-ttu-id="5ac77-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac77-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac77-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac77-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ac77-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5ac77-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac77-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ac77-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5ac77-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ac77-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac77-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac77-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac77-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac77-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="5ac77-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="5ac77-129">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="5ac77-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




