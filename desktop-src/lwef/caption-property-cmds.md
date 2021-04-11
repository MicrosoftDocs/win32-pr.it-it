---
title: Proprietà Caption (oggetto raccolta Commands)
description: Proprietà Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118794"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="fd275-103">Proprietà Caption (oggetto raccolta Commands)</span><span class="sxs-lookup"><span data-stu-id="fd275-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="fd275-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd275-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fd275-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fd275-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fd275-106">Determina il testo visualizzato per un oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="fd275-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd275-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="fd275-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fd275-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \* [Stringa Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="fd275-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="fd275-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fd275-109">Part</span></span>     | <span data-ttu-id="fd275-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd275-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="fd275-111">*string*</span><span class="sxs-lookup"><span data-stu-id="fd275-111">*string*</span></span> | <span data-ttu-id="fd275-112">Espressione stringa che restituisce il testo visualizzato come didascalia.</span><span class="sxs-lookup"><span data-stu-id="fd275-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd275-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd275-113">Remarks</span></span>

<span data-ttu-id="fd275-114">L'impostazione della proprietà [**Caption**](caption-property.md) per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) definisce la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su true e l'applicazione non è il client di input-Active.</span><span class="sxs-lookup"><span data-stu-id="fd275-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="fd275-115">Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="fd275-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="fd275-116">Se si definiscono comandi per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) con una [**didascalia**](caption-property.md), in genere si definisce anche una **didascalia** per la raccolta di **comandi** associati.</span><span class="sxs-lookup"><span data-stu-id="fd275-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
