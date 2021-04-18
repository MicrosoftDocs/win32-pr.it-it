---
title: EFFECTs. currentEffect
description: L'attributo currentEffect specifica o recupera la visualizzazione corrente.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325854"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="1260f-104">EFFECTs. currentEffect</span><span class="sxs-lookup"><span data-stu-id="1260f-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="1260f-105">L'attributo **currentEffect** specifica o recupera la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1260f-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="1260f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1260f-106">Possible Values</span></span>

<span data-ttu-id="1260f-107">Questo attributo è un **oggetto** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1260f-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="1260f-108">Il valore predefinito è la prima visualizzazione nell'ordine di creazione.</span><span class="sxs-lookup"><span data-stu-id="1260f-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="1260f-109">Se non è stata creata alcuna visualizzazione nell'interfaccia, il valore predefinito è la prima visualizzazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1260f-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="1260f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1260f-110">Remarks</span></span>

<span data-ttu-id="1260f-111">È possibile usare questo oggetto per accedere a visualizzazioni personalizzate create.</span><span class="sxs-lookup"><span data-stu-id="1260f-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="1260f-112">Ad esempio, è possibile esporre una proprietà tramite l'interfaccia **IDispatch** nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1260f-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="1260f-113">È quindi possibile modificare il valore della proprietà dall'interfaccia personalizzata rendendo la visualizzazione l'effetto corrente e quindi usando l'oggetto **currentEffect** per impostare un nuovo valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1260f-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="1260f-114">Se, ad esempio, la visualizzazione espone una proprietà denominata backgroundColor, il codice JScript seguente specifica un nuovo valore:</span><span class="sxs-lookup"><span data-stu-id="1260f-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="1260f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1260f-115">Requirements</span></span>



| <span data-ttu-id="1260f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1260f-116">Requirement</span></span> | <span data-ttu-id="1260f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1260f-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1260f-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1260f-118">Version</span></span><br/> | <span data-ttu-id="1260f-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1260f-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1260f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1260f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1260f-121">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="1260f-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="1260f-122">**EFFECTs. currentEffectTitle**</span><span class="sxs-lookup"><span data-stu-id="1260f-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="1260f-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="1260f-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





