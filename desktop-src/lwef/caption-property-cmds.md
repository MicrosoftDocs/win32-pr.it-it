---
title: Proprietà Caption (oggetto raccolta Commands)
description: Informazioni sulla proprietà Caption dell'oggetto Command Collection. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262053"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="8a9aa-104">Proprietà Caption (oggetto raccolta Commands)</span><span class="sxs-lookup"><span data-stu-id="8a9aa-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="8a9aa-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a9aa-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8a9aa-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8a9aa-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8a9aa-107">Determina il testo visualizzato per un [**oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="8a9aa-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="8a9aa-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8a9aa-109">*agent\***. Caratteri ("**_CharacterID_*_")._ \* [Stringa Commands.Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="8a9aa-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="8a9aa-110">Parte</span><span class="sxs-lookup"><span data-stu-id="8a9aa-110">Part</span></span>     | <span data-ttu-id="8a9aa-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a9aa-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="8a9aa-112">*string*</span><span class="sxs-lookup"><span data-stu-id="8a9aa-112">*string*</span></span> | <span data-ttu-id="8a9aa-113">Espressione stringa che restituisce il testo visualizzato come didascalia.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a9aa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a9aa-114">Remarks</span></span>

<span data-ttu-id="8a9aa-115">L'impostazione della proprietà [**Caption**](caption-property.md) per la raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) definisce come verrà visualizzato nel menu a comparsa del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su True e l'applicazione non è il client attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="8a9aa-116">Per specificare un tasto di scelta (mnemotico non inline) per **caption,** includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="8a9aa-117">Se si definiscono comandi per una [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) con [**una didascalia**](caption-property.md), in genere si definisce anche **una didascalia** per la raccolta **Commands** associata.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
