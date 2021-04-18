---
description: Specifica il tipo di conferma che può verificarsi in un oggetto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumerazione ConfirmationType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305686"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="9c16f-103">Enumerazione ConfirmationType</span><span class="sxs-lookup"><span data-stu-id="9c16f-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="9c16f-104">Specifica il tipo di conferma che può verificarsi in un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9c16f-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c16f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c16f-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="9c16f-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="9c16f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c16f-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ None**</span><span class="sxs-lookup"><span data-stu-id="9c16f-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="9c16f-108">Non viene applicata alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="9c16f-108">No confirmation is applied.</span></span> <span data-ttu-id="9c16f-109">[**IInkAnalyzer**](iinkanalyzer.md) è libero di modificare un nodo di contesto o uno qualsiasi dei relativi discendenti in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="9c16f-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="9c16f-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**\_NodeTypeAndProperties ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="9c16f-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="9c16f-111">[**IInkAnalyzer**](iinkanalyzer.md) non è in grado di modificare il tipo o qualsiasi proprietà del nodo di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="9c16f-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="9c16f-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType in \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="9c16f-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="9c16f-113">Il [**IInkAnalyzer**](iinkanalyzer.md) non eseguirà operazioni, tra cui l'aggiunta di input penna o l'Unione con altri [**ContextNode**](icontextnodes.md), che fanno sì che il bordo superiore venga spostato oltre il limite superiore corrente.</span><span class="sxs-lookup"><span data-stu-id="9c16f-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="9c16f-114">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9c16f-114">For example:</span></span>

-   <span data-ttu-id="9c16f-115">Un'applicazione analizza un set di input penna e viene identificato un ParagraphNode.</span><span class="sxs-lookup"><span data-stu-id="9c16f-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="9c16f-116">L'applicazione conferma il delimitatore di questo paragrafo.</span><span class="sxs-lookup"><span data-stu-id="9c16f-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="9c16f-117">L'utente dell'applicazione scrive nuovo input penna sopra il paragrafo corrente.</span><span class="sxs-lookup"><span data-stu-id="9c16f-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="9c16f-118">Quando l'analisi viene chiamata nuovamente, il nuovo input penna non verrà incorporato nel nodo di paragrafo confermato.</span><span class="sxs-lookup"><span data-stu-id="9c16f-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="9c16f-119">Poiché viene confermato solo il limite superiore, l'oggetto ContextNode può continuare ad aumentare in altre direzioni.</span><span class="sxs-lookup"><span data-stu-id="9c16f-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="9c16f-120">L'eliminazione dei tratti può causare lo spostamento del limite superiore.</span><span class="sxs-lookup"><span data-stu-id="9c16f-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="9c16f-121">La conversione dell'oggetto ContextNode può causare la modifica della posizione, ma non consente l'Unione di input penna aggiuntivi nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="9c16f-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="9c16f-122">Questo ConfirmationType è applicabile solo ai nodi di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="9c16f-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c16f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c16f-123">Remarks</span></span>

<span data-ttu-id="9c16f-124">È possibile usare il valore **NodeTypeAndProperties** solo per i nodi input penna e di disegno input penna (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="9c16f-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="9c16f-125">In caso contrario, viene restituito un **E \_ INVALIDARG** da [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="9c16f-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c16f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c16f-126">Requirements</span></span>



| <span data-ttu-id="9c16f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c16f-127">Requirement</span></span> | <span data-ttu-id="9c16f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9c16f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c16f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c16f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c16f-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9c16f-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c16f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c16f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c16f-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9c16f-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9c16f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c16f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c16f-134"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9c16f-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c16f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c16f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c16f-136">**IContextNode:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="9c16f-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="9c16f-137">**IContextNode:: deconfirmed**</span><span class="sxs-lookup"><span data-stu-id="9c16f-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




