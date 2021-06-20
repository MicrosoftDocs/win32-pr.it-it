---
title: Proprietà Enabled (oggetto Command)
description: Informazioni sulla proprietà dell'oggetto Comando abilitato. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407334"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="8e986-104">Proprietà Enabled (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="8e986-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="8e986-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e986-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8e986-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8e986-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8e986-107">Restituisce o imposta un valore che indica se **il comando** è abilitato nel menu a comparsa del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="8e986-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="8e986-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="8e986-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8e986-109">*agent\***. Caratteri ("**_CharacterID_*_"). Commands("_*_name_*_"). Valore_ \*  \[  =  *booleano abilitato*\]</span><span class="sxs-lookup"><span data-stu-id="8e986-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="8e986-110">Parte</span><span class="sxs-lookup"><span data-stu-id="8e986-110">Part</span></span>      | <span data-ttu-id="8e986-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e986-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e986-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="8e986-112">*boolean*</span></span> | <span data-ttu-id="8e986-113">Espressione booleana che specifica se **il comando è** abilitato.</span><span class="sxs-lookup"><span data-stu-id="8e986-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="8e986-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="8e986-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="8e986-115">Il **comando** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="8e986-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="8e986-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt></span><span class="sxs-lookup"><span data-stu-id="8e986-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="8e986-117">Il **comando** è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8e986-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e986-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e986-118">Remarks</span></span>

<span data-ttu-id="8e986-119">Se la [**proprietà Enabled**](enabled-property.md) è impostata su **True,** la didascalia dell'oggetto [**Command**](/windows/desktop/lwef/the-command-object) viene visualizzata come testo normale nel menu a comparsa del carattere quando l'applicazione client è attiva per l'input.</span><span class="sxs-lookup"><span data-stu-id="8e986-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="8e986-120">Se la **proprietà Enabled** è **False**, la didascalia viene visualizzata come testo non disponibile (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="8e986-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="8e986-121">Un comando **disabilitato non** è accessibile anche per l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="8e986-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

