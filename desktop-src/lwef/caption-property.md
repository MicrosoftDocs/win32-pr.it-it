---
title: Proprietà Caption (oggetto Command)
description: Informazioni sulla proprietà Caption dell'oggetto Command. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262553"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="2b171-104">Proprietà Caption (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="2b171-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="2b171-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2b171-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2b171-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2b171-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2b171-107">Determina il testo visualizzato per [**un oggetto Command**](/windows/desktop/lwef/the-command-object) nel menu a comparsa del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="2b171-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="2b171-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="2b171-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2b171-109">*agent\***. Caratteri ("**_CharacterID_*_"). Commands("_*_name_*_"). Stringa_ \*  \[  =  *didascalia*\]</span><span class="sxs-lookup"><span data-stu-id="2b171-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="2b171-110">Parte</span><span class="sxs-lookup"><span data-stu-id="2b171-110">Part</span></span>     | <span data-ttu-id="2b171-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b171-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b171-112">*string*</span><span class="sxs-lookup"><span data-stu-id="2b171-112">*string*</span></span> | <span data-ttu-id="2b171-113">Espressione stringa che restituisce il testo visualizzato come didascalia per **il comando**.</span><span class="sxs-lookup"><span data-stu-id="2b171-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b171-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b171-114">Remarks</span></span>

<span data-ttu-id="2b171-115">Per specificare un tasto di scelta (mnemotico non inline) per **caption**, includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="2b171-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="2b171-116">Se non si definisce **voiceCaption** per il comando, verrà usata l'impostazione **Didascalia.**</span><span class="sxs-lookup"><span data-stu-id="2b171-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
