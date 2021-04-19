---
title: AmbientAttributes. Visible
description: L'attributo Visible specifica o recupera la visibilità per il controllo.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes. Visible Media Player Windows
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331498"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="a94e9-104">AmbientAttributes. Visible</span><span class="sxs-lookup"><span data-stu-id="a94e9-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="a94e9-105">L'attributo **Visible** specifica o recupera la visibilità per il controllo.</span><span class="sxs-lookup"><span data-stu-id="a94e9-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="a94e9-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a94e9-106">Possible Values</span></span>

<span data-ttu-id="a94e9-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a94e9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a94e9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a94e9-108">Value</span></span> | <span data-ttu-id="a94e9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a94e9-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="a94e9-110">true</span><span class="sxs-lookup"><span data-stu-id="a94e9-110">true</span></span>  | <span data-ttu-id="a94e9-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a94e9-111">Default.</span></span> <span data-ttu-id="a94e9-112">Il controllo è visibile.</span><span class="sxs-lookup"><span data-stu-id="a94e9-112">The control is visible.</span></span> |
| <span data-ttu-id="a94e9-113">false</span><span class="sxs-lookup"><span data-stu-id="a94e9-113">false</span></span> | <span data-ttu-id="a94e9-114">Il controllo non è visibile.</span><span class="sxs-lookup"><span data-stu-id="a94e9-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="a94e9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a94e9-115">Remarks</span></span>

<span data-ttu-id="a94e9-116">Questo attributo è utile per nascondere i controlli, ad esempio quando si scambia un pulsante di sospensione per un pulsante Riproduci.</span><span class="sxs-lookup"><span data-stu-id="a94e9-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="a94e9-117">Se il valore è false, il controllo non è visibile e gli eventi click vengono passati al controllo sottostante.</span><span class="sxs-lookup"><span data-stu-id="a94e9-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="a94e9-118">Se il valore è true, il controllo è visibile e riceve l'evento Click stesso.</span><span class="sxs-lookup"><span data-stu-id="a94e9-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="a94e9-119">Il valore predefinito per l'elemento **automenu** è false.</span><span class="sxs-lookup"><span data-stu-id="a94e9-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="a94e9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a94e9-120">Requirements</span></span>



| <span data-ttu-id="a94e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94e9-121">Requirement</span></span> | <span data-ttu-id="a94e9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a94e9-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a94e9-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a94e9-123">Version</span></span><br/> | <span data-ttu-id="a94e9-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a94e9-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a94e9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a94e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94e9-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="a94e9-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





