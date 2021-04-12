---
title: Remove (metodo)
description: Remove (metodo)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337478"
---
# <a name="remove-method"></a><span data-ttu-id="7ccc0-103">Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="7ccc0-103">Remove Method</span></span>

<span data-ttu-id="7ccc0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ccc0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7ccc0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7ccc0-106">Rimuove un oggetto [**Command**](/windows/desktop/lwef/the-command-object) dalla raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7ccc0-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="7ccc0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7ccc0-108">*agente ***. Caratteri ("*** CharacterID ***"). Comandi. Rimuovi*** nome*</span><span class="sxs-lookup"><span data-stu-id="7ccc0-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="7ccc0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7ccc0-109">Part</span></span>   | <span data-ttu-id="7ccc0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ccc0-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="7ccc0-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="7ccc0-111">*Name*</span></span> | <span data-ttu-id="7ccc0-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-112">Required.</span></span> <span data-ttu-id="7ccc0-113">Valore stringa corrispondente all'ID per il comando.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ccc0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ccc0-114">Remarks</span></span>

<span data-ttu-id="7ccc0-115">Quando un oggetto [**comando**](/windows/desktop/lwef/the-command-object) viene rimosso dalla raccolta, non viene più visualizzato quando il menu popup del carattere viene visualizzato o nella finestra comandi quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ccc0-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7ccc0-116">See Also</span></span>

[<span data-ttu-id="7ccc0-117">**RemoveAll, metodo**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 