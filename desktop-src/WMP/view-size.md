---
title: Visualizza. size
description: Il metodo size ridimensiona la visualizzazione in un bordo specificato.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VISUALIZZAZIONE. dimensioni di Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325967"
---
# <a name="viewsize"></a><span data-ttu-id="29c07-104">Visualizza. size</span><span class="sxs-lookup"><span data-stu-id="29c07-104">VIEW.size</span></span>

<span data-ttu-id="29c07-105">Il metodo **size ridimensiona** la **visualizzazione** in un bordo specificato.</span><span class="sxs-lookup"><span data-stu-id="29c07-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="29c07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c07-107"><span id="handle"></span><span id="HANDLE"></span>*gestire*</span><span class="sxs-lookup"><span data-stu-id="29c07-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="29c07-108">Stringa che specifica il bordo o l'angolo da spostare durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="29c07-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="29c07-109">Questa stringa deve avere uno degli otto valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="29c07-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="29c07-110">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="29c07-110">Edge</span></span>   | <span data-ttu-id="29c07-111">Angolo</span><span class="sxs-lookup"><span data-stu-id="29c07-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="29c07-112">top</span><span class="sxs-lookup"><span data-stu-id="29c07-112">top</span></span>    | <span data-ttu-id="29c07-113">TopRight</span><span class="sxs-lookup"><span data-stu-id="29c07-113">topright</span></span>    |
| <span data-ttu-id="29c07-114">right</span><span class="sxs-lookup"><span data-stu-id="29c07-114">right</span></span>  | <span data-ttu-id="29c07-115">BottomRight</span><span class="sxs-lookup"><span data-stu-id="29c07-115">bottomright</span></span> |
| <span data-ttu-id="29c07-116">bottom</span><span class="sxs-lookup"><span data-stu-id="29c07-116">bottom</span></span> | <span data-ttu-id="29c07-117">BottomLeft</span><span class="sxs-lookup"><span data-stu-id="29c07-117">bottomleft</span></span>  |
| <span data-ttu-id="29c07-118">sinistro</span><span class="sxs-lookup"><span data-stu-id="29c07-118">left</span></span>   | <span data-ttu-id="29c07-119">TopLeft</span><span class="sxs-lookup"><span data-stu-id="29c07-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c07-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29c07-120">Return Value</span></span>

<span data-ttu-id="29c07-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="29c07-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29c07-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="29c07-122">Remarks</span></span>

<span data-ttu-id="29c07-123">Questo metodo viene in genere chiamato dall'interno di un gestore **OnMouseDown** .</span><span class="sxs-lookup"><span data-stu-id="29c07-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="29c07-124">Esegue il ridimensionamento quando il mouse viene trascinato e interrompe il ridimensionamento quando viene rilasciato il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="29c07-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="29c07-125">Se le dimensioni della **vista** sono limitate, non è possibile trascinare il mouse per ridimensionare la **visualizzazione** oltre i limiti limitati.</span><span class="sxs-lookup"><span data-stu-id="29c07-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="29c07-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="29c07-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="29c07-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29c07-127">Requirements</span></span>



| <span data-ttu-id="29c07-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="29c07-128">Requirement</span></span> | <span data-ttu-id="29c07-129">Valore</span><span class="sxs-lookup"><span data-stu-id="29c07-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="29c07-130">Versione</span><span class="sxs-lookup"><span data-stu-id="29c07-130">Version</span></span><br/> | <span data-ttu-id="29c07-131">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="29c07-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29c07-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29c07-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c07-133">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="29c07-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





