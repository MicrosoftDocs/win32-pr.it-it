---
title: Proprietà Visible (oggetto Commands)
description: Visible (proprietà)
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400164"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="5f278-103">Proprietà Visible (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="5f278-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="5f278-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f278-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5f278-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5f278-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5f278-106">Restituisce o imposta un valore che determina se la didascalia della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzata nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="5f278-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="5f278-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5f278-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="5f278-108">\*agente \***. Caratteri (**"\* CharacterID \*" \* *).* \*  \[  =  *Booleano* Commands. Visible\]</span><span class="sxs-lookup"><span data-stu-id="5f278-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="5f278-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5f278-109">Part</span></span>      | <span data-ttu-id="5f278-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f278-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f278-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="5f278-111">*boolean*</span></span> | <span data-ttu-id="5f278-112">Espressione booleana che specifica se l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="5f278-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="5f278-113">Valore **true** Viene visualizzata la didascalia.</span><span class="sxs-lookup"><span data-stu-id="5f278-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="5f278-114">**False** La didascalia non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="5f278-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f278-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f278-115">Remarks</span></span>

<span data-ttu-id="5f278-116">Per visualizzare la didascalia nel menu di scelta rapida del carattere quando l'applicazione non è il client input-attivo, questa proprietà deve essere impostata su **true** e la proprietà [**Caption**](caption-property.md) impostata per la raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="5f278-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="5f278-117">Inoltre, questa proprietà deve essere impostata su **true** per visualizzare i comandi della raccolta nel menu a comparsa quando l'applicazione è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="5f278-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

