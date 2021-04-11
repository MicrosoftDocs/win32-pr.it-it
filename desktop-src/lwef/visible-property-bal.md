---
title: Proprietà Visible (oggetto Balloon)
description: Visible (proprietà)
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047665"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="c6f9c-103">Proprietà Visible (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="c6f9c-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="c6f9c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6f9c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c6f9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c6f9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c6f9c-106">Restituisce o imposta l'impostazione visibile per la parola Balloon per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c6f9c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="c6f9c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="c6f9c-108">\*agente \***. Caratteri (**"\* CharacterID \*" \* *).* \*  \[  =  *Valore booleano* Balloon. Visible\]</span><span class="sxs-lookup"><span data-stu-id="c6f9c-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="c6f9c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c6f9c-109">Part</span></span>      | <span data-ttu-id="c6f9c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6f9c-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f9c-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="c6f9c-111">*boolean*</span></span> | <span data-ttu-id="c6f9c-112">Espressione booleana che specifica se la parola Balloon è visibile.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="c6f9c-113">Valore **true** Il fumetto è visibile.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="c6f9c-114">**False** Il fumetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6f9c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6f9c-115">Remarks</span></span>

<span data-ttu-id="c6f9c-116">Se si segue una chiamata [**Speak**](speak-method.md) o [**think**](think-method.md) con un'istruzione per tentare di modificare la proprietà del fumetto, potrebbe non influire sullo stato visibile del fumetto perché la chiamata **Speak** o **think** viene accodata, ma la chiamata non imposta lo stato visibile del fumetto.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="c6f9c-117">Pertanto, impostare questo valore solo quando nessuna chiamata a **Speak** o **think** si trova nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="c6f9c-118">Se si tenta di impostare questa proprietà quando il carattere è in conversazione, lo spostare o il trascinamento, l'impostazione della proprietà non diventa effettiva fino al completamento dell'operazione precedente.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="c6f9c-119">La chiamata ai metodi [**Speak**](speak-method.md) e [**think**](think-method.md) rende automaticamente visibile il fumetto, impostando la proprietà [**Visible**](visible-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="c6f9c-120">Se la proprietà Nascondi automaticamente del fumetto del carattere è abilitata, il fumetto viene nascosto automaticamente dopo la pronuncia del testo di output.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="c6f9c-121">Quando si fa clic o si trascina un carattere che non è in corso di conversazione, il fumetto viene nascosto automaticamente anche se l'impostazione Nascondi automaticamente è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="c6f9c-122">È possibile modificare l'impostazione Nascondi automaticamente del carattere usando la proprietà [**Style**](style-property.md) del fumetto.</span><span class="sxs-lookup"><span data-stu-id="c6f9c-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="c6f9c-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c6f9c-123">See Also</span></span>

[<span data-ttu-id="c6f9c-124">**Style (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="c6f9c-124">**Style property**</span></span>](style-property.md)


 

 





