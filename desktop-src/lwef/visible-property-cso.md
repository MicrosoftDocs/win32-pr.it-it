---
title: Proprietà Visible (oggetto Commands)
description: Informazioni sulla proprietà Visible dell'oggetto Commands, che determina se la didascalia della raccolta Commands viene visualizzata nel menu a comparsa del carattere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396256"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="af149-103">Proprietà Visible (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="af149-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="af149-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af149-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af149-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="af149-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af149-106">Restituisce o imposta un valore che determina se la didascalia della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzata nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="af149-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="af149-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="af149-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="af149-108">*agent\***. Characters(**"* CharacterID *"\*\*). Valore booleano Commands.Visible* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="af149-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="af149-109">Parte</span><span class="sxs-lookup"><span data-stu-id="af149-109">Part</span></span>      | <span data-ttu-id="af149-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af149-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af149-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="af149-111">*boolean*</span></span> | <span data-ttu-id="af149-112">Espressione booleana che specifica se [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzato nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="af149-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="af149-113">**True** Viene visualizzata la didascalia.</span><span class="sxs-lookup"><span data-stu-id="af149-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="af149-114">**False** La didascalia non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="af149-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af149-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="af149-115">Remarks</span></span>

<span data-ttu-id="af149-116">Perché la didascalia venga visualizzata nel menu a comparsa del carattere quando l'applicazione non è il client attivo per l'input, questa proprietà deve essere impostata su **True** e la proprietà [**Caption**](caption-property.md) deve essere impostata per la raccolta Commands.</span><span class="sxs-lookup"><span data-stu-id="af149-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="af149-117">Inoltre, questa proprietà deve essere impostata su **True** perché i comandi nella raccolta vengano visualizzati nel menu a comparsa quando l'applicazione è attiva per l'input.</span><span class="sxs-lookup"><span data-stu-id="af149-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

