---
title: AmbientAttributes. alphaBlend
description: L'attributo alphaBlend specifica o recupera un valore per la fusione alfa di qualsiasi visualizzazione, sottovista o widget dell'interfaccia utente.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Media Player Windows AmbientAttributes. alphaBlend
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331411"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="1df51-104">AmbientAttributes. alphaBlend</span><span class="sxs-lookup"><span data-stu-id="1df51-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="1df51-105">L'attributo **alphaBlend** specifica o recupera un valore per la fusione alfa di qualsiasi **visualizzazione**, **sottovista** o widget dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1df51-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="1df51-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1df51-106">Possible Values</span></span>

<span data-ttu-id="1df51-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore compreso tra 0 (nessuna opacità) e 255 (opacità completa) e un valore predefinito pari a 255.</span><span class="sxs-lookup"><span data-stu-id="1df51-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df51-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1df51-108">Remarks</span></span>

<span data-ttu-id="1df51-109">Questo attributo consente la visualizzazione di un elemento semitrasparente, a seconda della quantità di set di opacità.</span><span class="sxs-lookup"><span data-stu-id="1df51-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="1df51-110">Meno opacità, più trasparente verrà visualizzato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1df51-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="1df51-111">Ogni elemento nell'interfaccia può avere un valore di opacità separato, ad eccezione degli elementi Button in un controllo **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="1df51-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="1df51-112">Quando **alphaBlend** è impostato in **visualizzazione**, viene impostata l'opacità dell'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1df51-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="1df51-113">Alpha Blend non funzionerà per i controlli finestra, tra cui **playlist**, **Effects**, **ListBox**, **popup**, **casella** e **video** (se la **finestra** è impostata su false).</span><span class="sxs-lookup"><span data-stu-id="1df51-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="1df51-114">Quando **alphaBlend** è impostato su **View**, l'intera interfaccia diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="1df51-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="1df51-115">Gli attributi **transparencyColor** usati da diversi elementi non sono supportati con **alphaBlend**.</span><span class="sxs-lookup"><span data-stu-id="1df51-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="1df51-116">Quando si usa **alphaBlend** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero.</span><span class="sxs-lookup"><span data-stu-id="1df51-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="1df51-117">Se il colore di primo piano è anche nero (ovvero il valore predefinito per il *testo*.**foregroundColor**), il testo potrebbe diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="1df51-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="1df51-118">Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.</span><span class="sxs-lookup"><span data-stu-id="1df51-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="1df51-119">Questo attributo non è supportato in Windows 98.</span><span class="sxs-lookup"><span data-stu-id="1df51-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1df51-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1df51-120">Requirements</span></span>



| <span data-ttu-id="1df51-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df51-121">Requirement</span></span> | <span data-ttu-id="1df51-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1df51-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1df51-123">Versione</span><span class="sxs-lookup"><span data-stu-id="1df51-123">Version</span></span><br/> | <span data-ttu-id="1df51-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1df51-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1df51-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1df51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df51-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="1df51-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1df51-127">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="1df51-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="1df51-128">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="1df51-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="1df51-129">**TESTO. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="1df51-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="1df51-130">**TESTO. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="1df51-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





