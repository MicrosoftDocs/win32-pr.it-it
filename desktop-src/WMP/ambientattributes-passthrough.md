---
title: AmbientAttributes. passThrough
description: L'attributo passThrough specifica o recupera un valore che indica se il controllo passerà tutti gli eventi del mouse al controllo sottostante.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Media Player Windows AmbientAttributes. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326029"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="8b046-104">AmbientAttributes. passThrough</span><span class="sxs-lookup"><span data-stu-id="8b046-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="8b046-105">L'attributo **passThrough** specifica o recupera un valore che indica se il controllo passerà tutti gli eventi del mouse al controllo sottostante.</span><span class="sxs-lookup"><span data-stu-id="8b046-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="8b046-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8b046-106">Possible Values</span></span>

<span data-ttu-id="8b046-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8b046-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="8b046-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8b046-108">Value</span></span> | <span data-ttu-id="8b046-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b046-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="8b046-110">true</span><span class="sxs-lookup"><span data-stu-id="8b046-110">true</span></span>  | <span data-ttu-id="8b046-111">Il controllo passa gli eventi al controllo al suo interno.</span><span class="sxs-lookup"><span data-stu-id="8b046-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="8b046-112">false</span><span class="sxs-lookup"><span data-stu-id="8b046-112">false</span></span> | <span data-ttu-id="8b046-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8b046-113">Default.</span></span> <span data-ttu-id="8b046-114">Il controllo non passa gli eventi tramite.</span><span class="sxs-lookup"><span data-stu-id="8b046-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="8b046-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b046-115">Remarks</span></span>

<span data-ttu-id="8b046-116">Questo attributo è utile se, ad esempio, un controllo di testo si trova sopra un controllo Button solo per fornire l'etichettatura.</span><span class="sxs-lookup"><span data-stu-id="8b046-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="8b046-117">In questo caso, i clic sul controllo di testo devono essere passati al controllo Button.</span><span class="sxs-lookup"><span data-stu-id="8b046-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="8b046-118">L'attributo **passThrough** non è supportato dagli elementi **VIEW**, **subview** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="8b046-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="8b046-119">Non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se *Effects*. **windowed** è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="8b046-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b046-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b046-120">Requirements</span></span>



| <span data-ttu-id="8b046-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b046-121">Requirement</span></span> | <span data-ttu-id="8b046-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8b046-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8b046-123">Versione</span><span class="sxs-lookup"><span data-stu-id="8b046-123">Version</span></span><br/> | <span data-ttu-id="8b046-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="8b046-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b046-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b046-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b046-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="8b046-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





