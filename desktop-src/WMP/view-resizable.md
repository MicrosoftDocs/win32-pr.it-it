---
title: Visualizza. ridimensionabile
description: L'attributo ridimensionabile recupera un valore che indica se la vista può essere ridimensionata.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Visualizza. Media Player di Windows ridimensionabili
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324070"
---
# <a name="viewresizable"></a><span data-ttu-id="87179-104">Visualizza. ridimensionabile</span><span class="sxs-lookup"><span data-stu-id="87179-104">VIEW.resizable</span></span>

<span data-ttu-id="87179-105">L'attributo **ridimensionabile** recupera un valore che indica se la **vista** può essere ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="87179-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="87179-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="87179-106">Possible Values</span></span>

<span data-ttu-id="87179-107">Questo attributo è un valore **booleano** di sola lettura con un valore predefinito uguale all'attributo della **barra** del titolo.</span><span class="sxs-lookup"><span data-stu-id="87179-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="87179-108">Valori</span><span class="sxs-lookup"><span data-stu-id="87179-108">Values</span></span> | <span data-ttu-id="87179-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87179-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="87179-110">true</span><span class="sxs-lookup"><span data-stu-id="87179-110">true</span></span>   | <span data-ttu-id="87179-111">La visualizzazione può essere ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="87179-111">View can be resized.</span></span>    |
| <span data-ttu-id="87179-112">false</span><span class="sxs-lookup"><span data-stu-id="87179-112">false</span></span>  | <span data-ttu-id="87179-113">Impossibile ridimensionare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="87179-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="87179-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="87179-114">Remarks</span></span>

<span data-ttu-id="87179-115">Se non è presente alcuna **barra** di titolo e pertanto nessuna finestra o bordo, è necessario usare il metodo **size** per ridimensionare l'elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="87179-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="87179-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87179-116">Requirements</span></span>



| <span data-ttu-id="87179-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87179-117">Requirement</span></span> | <span data-ttu-id="87179-118">Valore</span><span class="sxs-lookup"><span data-stu-id="87179-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="87179-119">Versione</span><span class="sxs-lookup"><span data-stu-id="87179-119">Version</span></span><br/> | <span data-ttu-id="87179-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="87179-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87179-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87179-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87179-122">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="87179-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





