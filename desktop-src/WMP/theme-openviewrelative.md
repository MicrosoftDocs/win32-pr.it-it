---
title: THEME. openViewRelative
description: Il metodo openViewRelative apre una visualizzazione in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME. openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328390"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="ba71a-104">THEME. openViewRelative</span><span class="sxs-lookup"><span data-stu-id="ba71a-104">THEME.openViewRelative</span></span>

<span data-ttu-id="ba71a-105">Il metodo **openViewRelative** apre una **visualizzazione** in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba71a-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="ba71a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba71a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba71a-107"><span id="view"></span><span id="VIEW"></span>*visualizzare*</span><span class="sxs-lookup"><span data-stu-id="ba71a-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="ba71a-108">**Stringa** che specifica l' **ID** della **visualizzazione** da aprire.</span><span class="sxs-lookup"><span data-stu-id="ba71a-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="ba71a-109"><span id="left"></span><span id="LEFT"></span>*sinistra*</span><span class="sxs-lookup"><span data-stu-id="ba71a-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="ba71a-110">**Numero** (**Long**) che specifica la distanza iniziale, in pixel, del bordo sinistro della **visualizzazione** dal bordo sinistro dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba71a-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="ba71a-111">Un valore negativo indica una posizione iniziale a sinistra del bordo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba71a-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="ba71a-112"><span id="top"></span><span id="TOP"></span>*In alto*</span><span class="sxs-lookup"><span data-stu-id="ba71a-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="ba71a-113">**Numero** (**Long**) che specifica la posizione iniziale del bordo superiore della **visualizzazione** rispetto al bordo superiore dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba71a-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="ba71a-114">Un valore negativo indica una posizione iniziale sopra il bordo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba71a-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba71a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba71a-115">Return Value</span></span>

<span data-ttu-id="ba71a-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ba71a-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba71a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba71a-117">Remarks</span></span>

<span data-ttu-id="ba71a-118">La posizione specificata per la **visualizzazione** viene utilizzata la prima volta che viene chiamato questo metodo, dopo il quale l'utente può trascinare la **visualizzazione** in un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="ba71a-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="ba71a-119">La nuova posizione viene salvata e, nelle chiamate successive, viene usata la posizione più recente.</span><span class="sxs-lookup"><span data-stu-id="ba71a-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="ba71a-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="ba71a-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="ba71a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba71a-121">Requirements</span></span>



| <span data-ttu-id="ba71a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba71a-122">Requirement</span></span> | <span data-ttu-id="ba71a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ba71a-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ba71a-124">Versione</span><span class="sxs-lookup"><span data-stu-id="ba71a-124">Version</span></span><br/> | <span data-ttu-id="ba71a-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ba71a-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba71a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba71a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba71a-127">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="ba71a-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="ba71a-128">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="ba71a-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="ba71a-129">**TEMA. openView**</span><span class="sxs-lookup"><span data-stu-id="ba71a-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





