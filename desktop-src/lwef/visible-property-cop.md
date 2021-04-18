---
title: Proprietà Visible (oggetto Command)
description: Visible (proprietà)
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300726"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="f3e14-103">Proprietà Visible (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="f3e14-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="f3e14-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3e14-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f3e14-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f3e14-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f3e14-106">Restituisce o imposta un valore che indica se il [**comando**](/windows/desktop/lwef/the-command-object) è visibile nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="f3e14-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f3e14-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="f3e14-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="f3e14-108">\*agente \***. Caratteri (**"\* CharacterID *"**). Comandi (**"* nome \*" \* *).* \*  \[  =  *Valore booleano* visibile\]</span><span class="sxs-lookup"><span data-stu-id="f3e14-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="f3e14-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f3e14-109">Part</span></span>      | <span data-ttu-id="f3e14-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3e14-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e14-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f3e14-111">*boolean*</span></span> | <span data-ttu-id="f3e14-112">Espressione booleana che specifica se la didascalia del [**comando**](/windows/desktop/lwef/the-command-object)viene visualizzata nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="f3e14-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="f3e14-113">**True** (impostazione predefinita) viene visualizzata la didascalia.</span><span class="sxs-lookup"><span data-stu-id="f3e14-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="f3e14-114">**False** La didascalia non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="f3e14-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3e14-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3e14-115">Remarks</span></span>

<span data-ttu-id="f3e14-116">Impostare questa proprietà su **false** se si desidera includere l'input vocale per le interfacce personali senza visualizzarlo nel menu a comparsa per il carattere.</span><span class="sxs-lookup"><span data-stu-id="f3e14-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="f3e14-117">Se si imposta la proprietà [**Caption**](caption-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) sulla stringa vuota (""), il testo della didascalia non verrà visualizzato nel menu di scelta rapida (ad esempio, come riga vuota), indipendentemente dalla relativa impostazione della proprietà [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e14-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="f3e14-118">L'impostazione della proprietà [**Visible**](visible-property.md) della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) padre di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) non influisce sull'impostazione della proprietà **Visible** del **comando**.</span><span class="sxs-lookup"><span data-stu-id="f3e14-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

