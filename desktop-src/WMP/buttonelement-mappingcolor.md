---
title: BUTTONelement. mappingColor
description: L'attributo mappingColor specifica o recupera la chiave di colore che identifica questo BUTTONelement in BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONelement. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325002"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="74bb2-104">BUTTONelement. mappingColor</span><span class="sxs-lookup"><span data-stu-id="74bb2-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="74bb2-105">L'attributo **mappingColor** specifica o recupera la chiave di colore che identifica questo **ButtonElement** in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="74bb2-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="74bb2-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="74bb2-106">Possible Values</span></span>

<span data-ttu-id="74bb2-107">Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="74bb2-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="74bb2-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="74bb2-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74bb2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="74bb2-109">Remarks</span></span>

<span data-ttu-id="74bb2-110">Questo attributo specifica il colore dell'area nel gruppo di pulsanti **mappingImage** che corrisponde a questo elemento Button.</span><span class="sxs-lookup"><span data-stu-id="74bb2-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="74bb2-111">Tutti i clic su questa area vengono gestiti da questo elemento Button.</span><span class="sxs-lookup"><span data-stu-id="74bb2-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="74bb2-112">Se viene specificato un colore non valido, il **pulsante** non viene attivato.</span><span class="sxs-lookup"><span data-stu-id="74bb2-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="74bb2-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="74bb2-113">Examples</span></span>

<span data-ttu-id="74bb2-114">L'esempio seguente è un file di definizione dell'interfaccia completa che illustra come vengono usati alcuni degli attributi **ButtonElement** .</span><span class="sxs-lookup"><span data-stu-id="74bb2-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="74bb2-115">Si trova nella directory degli esempi installata con l'SDK.</span><span class="sxs-lookup"><span data-stu-id="74bb2-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="74bb2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74bb2-116">Requirements</span></span>



| <span data-ttu-id="74bb2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bb2-117">Requirement</span></span> | <span data-ttu-id="74bb2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="74bb2-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="74bb2-119">Versione</span><span class="sxs-lookup"><span data-stu-id="74bb2-119">Version</span></span><br/> | <span data-ttu-id="74bb2-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="74bb2-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74bb2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74bb2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bb2-122">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="74bb2-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="74bb2-123">**BUTTONelement (elemento)**</span><span class="sxs-lookup"><span data-stu-id="74bb2-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="74bb2-124">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="74bb2-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





