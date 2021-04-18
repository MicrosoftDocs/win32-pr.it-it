---
title: Proprietà Enabled (oggetto Balloon)
description: Proprietà Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300830"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="3cf58-103">Proprietà Enabled (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="3cf58-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="3cf58-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cf58-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3cf58-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3cf58-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3cf58-106">Restituisce un valore che indica se la parola Balloon è abilitata per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="3cf58-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3cf58-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="3cf58-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3cf58-108">\*agente \***. Caratteri ("**_CharacterID_*_"). Balloon. Enabled_*</span><span class="sxs-lookup"><span data-stu-id="3cf58-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="3cf58-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3cf58-109">Value</span></span>     | <span data-ttu-id="3cf58-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cf58-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="3cf58-111">**True**</span><span class="sxs-lookup"><span data-stu-id="3cf58-111">**True**</span></span>  | <span data-ttu-id="3cf58-112">Il fumetto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3cf58-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="3cf58-113">**False**</span><span class="sxs-lookup"><span data-stu-id="3cf58-113">**False**</span></span> | <span data-ttu-id="3cf58-114">Il fumetto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="3cf58-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cf58-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cf58-115">Remarks</span></span>

<span data-ttu-id="3cf58-116">La proprietà **Enabled** restituisce un valore booleano che specifica se il fumetto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3cf58-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="3cf58-117">Lo stato predefinito del fumetto di Word viene impostato come parte della definizione di un carattere quando il carattere viene compilato nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3cf58-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3cf58-118">Se un carattere è definito in modo da non supportare la parola Balloon, questa proprietà sarà sempre **false** per il carattere.</span><span class="sxs-lookup"><span data-stu-id="3cf58-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




