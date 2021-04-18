---
title: Proprietà Enabled (oggetto Command)
description: Proprietà Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300831"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="e74b1-103">Proprietà Enabled (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="e74b1-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="e74b1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e74b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e74b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e74b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e74b1-106">Restituisce o imposta un valore che indica se il **comando** è abilitato nel menu di scelta rapida del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="e74b1-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="e74b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="e74b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e74b1-108">\*agente \***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_Name_\*_")._ \*  \[  =  *Valore booleano* abilitato\]</span><span class="sxs-lookup"><span data-stu-id="e74b1-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="e74b1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e74b1-109">Part</span></span>      | <span data-ttu-id="e74b1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e74b1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e74b1-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e74b1-111">*boolean*</span></span> | <span data-ttu-id="e74b1-112">Espressione booleana che specifica se il **comando** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e74b1-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="e74b1-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="e74b1-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="e74b1-114">Il **comando** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e74b1-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="e74b1-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="e74b1-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="e74b1-116">Il **comando** è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e74b1-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e74b1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e74b1-117">Remarks</span></span>

<span data-ttu-id="e74b1-118">Se la proprietà [**Enabled**](enabled-property.md) è impostata su **true**, la didascalia degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) viene visualizzata come testo normale nel menu popup del carattere quando l'applicazione client è di tipo input-attivo.</span><span class="sxs-lookup"><span data-stu-id="e74b1-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="e74b1-119">Se la proprietà **Enabled** è **false**, la didascalia viene visualizzata come testo non disponibile (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="e74b1-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="e74b1-120">Non è inoltre possibile accedere a un **comando** disabilitato per l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="e74b1-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

