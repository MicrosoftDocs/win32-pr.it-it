---
title: Proprietà Caption (oggetto Command)
description: Proprietà Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300798"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="64683-103">Proprietà Caption (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="64683-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="64683-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64683-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="64683-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="64683-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="64683-106">Determina il testo visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object) nel menu di scelta rapida del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="64683-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="64683-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="64683-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="64683-108">\*agente \***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_Name_\*_"). Stringa didascalia_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="64683-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="64683-109">Parte</span><span class="sxs-lookup"><span data-stu-id="64683-109">Part</span></span>     | <span data-ttu-id="64683-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64683-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64683-111">*string*</span><span class="sxs-lookup"><span data-stu-id="64683-111">*string*</span></span> | <span data-ttu-id="64683-112">Espressione stringa che restituisce il testo visualizzato come didascalia per il **comando**.</span><span class="sxs-lookup"><span data-stu-id="64683-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64683-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="64683-113">Remarks</span></span>

<span data-ttu-id="64683-114">Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="64683-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="64683-115">Se non si definisce un **VoiceCaption** per il comando, verrà usata l'impostazione della **didascalia** .</span><span class="sxs-lookup"><span data-stu-id="64683-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
