---
title: Proprietà confidenza
description: Proprietà confidenza
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398886"
---
# <a name="confidence-property"></a><span data-ttu-id="37e5c-103">Proprietà confidenza</span><span class="sxs-lookup"><span data-stu-id="37e5c-103">Confidence Property</span></span>

<span data-ttu-id="37e5c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37e5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="37e5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="37e5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="37e5c-106">Restituisce o imposta un valore che indica se la **confidenza** del client viene visualizzata nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="37e5c-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="37e5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="37e5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="37e5c-108">\*agente ***. Caratteri ("*** CharacterID ***"). Comandi ("*** Name \***")**. \* \*\* \*  \[  =  *numero* di confidenza\]</span><span class="sxs-lookup"><span data-stu-id="37e5c-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="37e5c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="37e5c-109">Part</span></span>     | <span data-ttu-id="37e5c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37e5c-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e5c-111">*Number*</span><span class="sxs-lookup"><span data-stu-id="37e5c-111">*Number*</span></span> | <span data-ttu-id="37e5c-112">Espressione numerica che restituisce un valore long integer che identifica il valore di confidenza per il [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="37e5c-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37e5c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="37e5c-113">Remarks</span></span>

<span data-ttu-id="37e5c-114">Se il valore di confidenza restituito della corrispondenza migliore (UserInput. Confidence) non supera il valore impostato per la proprietà **confidenza** , il testo fornito in [**ConfidenceText**](confidencetext-property.md) viene visualizzato nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="37e5c-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 