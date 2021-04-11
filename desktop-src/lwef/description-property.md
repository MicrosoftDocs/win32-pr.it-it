---
title: Proprietà Description (funzionalità legacy dell'ambiente Windows)
description: Proprietà Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047696"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="42bc9-103">Proprietà Description (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="42bc9-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="42bc9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42bc9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="42bc9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="42bc9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42bc9-106">Restituisce o imposta una stringa che specifica la descrizione per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="42bc9-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="42bc9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="42bc9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="42bc9-108">*agente*. **Caratteri ("**_CharacterID_*_")._* \[  =  *Stringa* di descrizione\]</span><span class="sxs-lookup"><span data-stu-id="42bc9-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="42bc9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="42bc9-109">Part</span></span>     | <span data-ttu-id="42bc9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42bc9-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bc9-111">*string*</span><span class="sxs-lookup"><span data-stu-id="42bc9-111">*string*</span></span> | <span data-ttu-id="42bc9-112">Valore stringa corrispondente alla descrizione del carattere (nell'impostazione della lingua corrente).</span><span class="sxs-lookup"><span data-stu-id="42bc9-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42bc9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="42bc9-113">Remarks</span></span>

<span data-ttu-id="42bc9-114">La **Descrizione** di un carattere può dipendere dall'impostazione **LanguageID** del carattere.</span><span class="sxs-lookup"><span data-stu-id="42bc9-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="42bc9-115">Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a un altro.</span><span class="sxs-lookup"><span data-stu-id="42bc9-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="42bc9-116">La **Descrizione** predefinita del carattere per una lingua specifica viene definita quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="42bc9-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="42bc9-117">L'impostazione della proprietà **Description** è facoltativa e non può essere specificata per tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="42bc9-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




