---
title: Proprietà Enabled (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto Enabled Balloon. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407304"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="9acba-104">Proprietà Enabled (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="9acba-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="9acba-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9acba-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9acba-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9acba-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9acba-107">Restituisce un valore che indica se il fumetto è abilitato per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="9acba-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9acba-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="9acba-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9acba-109">*agent\***. Caratteri ("**_CharacterID_*_"). Balloon.Enabled_\*</span><span class="sxs-lookup"><span data-stu-id="9acba-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="9acba-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9acba-110">Value</span></span>     | <span data-ttu-id="9acba-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9acba-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="9acba-112">**True**</span><span class="sxs-lookup"><span data-stu-id="9acba-112">**True**</span></span>  | <span data-ttu-id="9acba-113">Il balloon è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9acba-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="9acba-114">**False**</span><span class="sxs-lookup"><span data-stu-id="9acba-114">**False**</span></span> | <span data-ttu-id="9acba-115">Il balloon è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9acba-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9acba-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9acba-116">Remarks</span></span>

<span data-ttu-id="9acba-117">La **proprietà Enabled** restituisce un valore booleano che specifica se il balloon è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9acba-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="9acba-118">Lo stato predefinito del fumetto viene impostato come parte della definizione di un carattere quando il carattere viene compilato nell'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9acba-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9acba-119">Se un carattere è definito per non supportare il fumetto, questa proprietà sarà sempre **False** per il carattere.</span><span class="sxs-lookup"><span data-stu-id="9acba-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




