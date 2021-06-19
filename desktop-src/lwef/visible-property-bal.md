---
title: Proprietà Visible (oggetto Balloon)
description: Informazioni sulla proprietà Visible dell'oggetto Balloon, che restituisce o imposta l'impostazione visibile per il fumetto per il carattere specificato.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396326"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="ecd6d-103">Proprietà Visible (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="ecd6d-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="ecd6d-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ecd6d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ecd6d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ecd6d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ecd6d-106">Restituisce o imposta l'impostazione visibile per il fumetto per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="ecd6d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ecd6d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="ecd6d-108">*agent\***. Characters(**"* CharacterID *"\*\*). Booleano Balloon.Visible* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="ecd6d-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="ecd6d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ecd6d-109">Part</span></span>      | <span data-ttu-id="ecd6d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecd6d-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd6d-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="ecd6d-111">*boolean*</span></span> | <span data-ttu-id="ecd6d-112">Espressione booleana che specifica se il fumetto della parola è visibile.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="ecd6d-113">**True** Il fumetto è visibile.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="ecd6d-114">**False** Il fumetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecd6d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecd6d-115">Remarks</span></span>

<span data-ttu-id="ecd6d-116">Se si segue una chiamata [**Speak**](speak-method.md) o Think con un'istruzione per tentare di modificare la proprietà del fumetto, potrebbe non influire sullo stato Visible del fumetto perché la chiamata **Speak** o [**Think**](think-method.md) viene accodata, ma la chiamata che imposta lo stato visibile del fumetto non lo fa. </span><span class="sxs-lookup"><span data-stu-id="ecd6d-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="ecd6d-117">Pertanto, impostare questo valore solo quando nessuna **chiamata Speak** o **Think** è presente nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="ecd6d-118">Se si tenta di impostare questa proprietà mentre il carattere parla, si sposta o viene trascinato, l'impostazione della proprietà non ha effetto fino al completamento dell'operazione precedente.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="ecd6d-119">La chiamata [**dei metodi Speak**](speak-method.md) e [**Think**](think-method.md) rende automaticamente visibile il fumetto, impostando la [**proprietà Visible**](visible-property.md) su **True.**</span><span class="sxs-lookup"><span data-stu-id="ecd6d-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="ecd6d-120">Se la proprietà AutoHide del fumetto del carattere è abilitata, il fumetto viene automaticamente nascosto dopo la pronuncia del testo di output.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="ecd6d-121">Se si fa clic o si trascina un carattere che attualmente non parla, il fumetto viene nascosto automaticamente anche se l'impostazione Nascondi automaticamente è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ecd6d-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="ecd6d-122">È possibile modificare l'impostazione AutoHide del carattere usando la proprietà [**Style del fumetto.**](style-property.md)</span><span class="sxs-lookup"><span data-stu-id="ecd6d-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="ecd6d-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ecd6d-123">See Also</span></span>

[<span data-ttu-id="ecd6d-124">**Style - proprietà**</span><span class="sxs-lookup"><span data-stu-id="ecd6d-124">**Style property**</span></span>](style-property.md)


 

 





