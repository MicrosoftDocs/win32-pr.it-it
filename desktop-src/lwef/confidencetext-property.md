---
title: Proprietà ConfidenceText
description: Proprietà ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398949"
---
# <a name="confidencetext-property"></a><span data-ttu-id="99f2e-103">Proprietà ConfidenceText</span><span class="sxs-lookup"><span data-stu-id="99f2e-103">ConfidenceText Property</span></span>

<span data-ttu-id="99f2e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99f2e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="99f2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="99f2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="99f2e-106">Restituisce o imposta il **ConfidenceText** del client visualizzato nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="99f2e-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="99f2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="99f2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="99f2e-108">\* Agent ***. Caratteri ("*** CharacterID ***"). Comandi ("*** nome \***")**.  \[ ConfidenceText  =  *stringa* di\]</span><span class="sxs-lookup"><span data-stu-id="99f2e-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="99f2e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="99f2e-109">Part</span></span>     | <span data-ttu-id="99f2e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99f2e-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f2e-111">*string*</span><span class="sxs-lookup"><span data-stu-id="99f2e-111">*string*</span></span> | <span data-ttu-id="99f2e-112">Espressione stringa che restituisce il testo per **ConfidenceText** per il [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="99f2e-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99f2e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="99f2e-113">Remarks</span></span>

<span data-ttu-id="99f2e-114">Quando il valore di confidenza restituito della corrispondenza migliore (UserInput. Confidence) non supera l'impostazione di [**attendibilità**](confidence-property.md) , nel server viene visualizzato il testo fornito in **ConfidenceText** nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="99f2e-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 