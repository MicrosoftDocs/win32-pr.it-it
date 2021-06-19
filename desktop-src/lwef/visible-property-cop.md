---
title: Proprietà Visible (oggetto Command)
description: Informazioni sulla proprietà Visible dell'oggetto Command, che restituisce o imposta se il comando è visibile nel menu a comparsa del carattere.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396246"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="62186-103">Proprietà Visible (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="62186-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="62186-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62186-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="62186-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="62186-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="62186-106">Restituisce o imposta un [**valore che**](/windows/desktop/lwef/the-command-object) indica se il comando è visibile nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="62186-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="62186-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="62186-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="62186-108">*agent\***. Characters(**"* CharacterID *"**). Commands(**"* name *"\*\*). Valore* \*  \[  =  *booleano visibile*\]</span><span class="sxs-lookup"><span data-stu-id="62186-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="62186-109">Parte</span><span class="sxs-lookup"><span data-stu-id="62186-109">Part</span></span>      | <span data-ttu-id="62186-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62186-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62186-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="62186-111">*boolean*</span></span> | <span data-ttu-id="62186-112">Espressione booleana che specifica se [**la**](/windows/desktop/lwef/the-command-object)didascalia del comando viene visualizzata nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="62186-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="62186-113">**True** (impostazione predefinita) Viene visualizzata la didascalia.</span><span class="sxs-lookup"><span data-stu-id="62186-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="62186-114">**False** La didascalia non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="62186-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62186-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62186-115">Remarks</span></span>

<span data-ttu-id="62186-116">Impostare questa proprietà **su False** quando si vuole includere l'input vocale per le proprie interfacce senza che vengano visualizzate nel menu a comparsa per il carattere.</span><span class="sxs-lookup"><span data-stu-id="62186-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="62186-117">Se si imposta la proprietà [**Caption**](caption-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) sulla stringa vuota (""), il testo della didascalia non verrà visualizzato nel menu a comparsa ,ad esempio come riga vuota, indipendentemente dall'impostazione della proprietà [**Visible.**](visible-property.md)</span><span class="sxs-lookup"><span data-stu-id="62186-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="62186-118">[**L'impostazione**](visible-property.md) della proprietà [**Visible della raccolta Commands**](/windows/desktop/lwef/the-command-object) padre di un oggetto [**Command**](/windows/desktop/lwef/the-commands-collection-object) non influisce sull'impostazione della proprietà **Visible** di **Command.**</span><span class="sxs-lookup"><span data-stu-id="62186-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

