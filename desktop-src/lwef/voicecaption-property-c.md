---
title: Proprietà VoiceCaption (oggetto Command)
description: Informazioni sulla proprietà VoiceCaption dell'oggetto Command, che imposta o restituisce il testo visualizzato per l'oggetto Command nella finestra Comandi vocali.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396166"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="a35a1-103">Proprietà VoiceCaption (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="a35a1-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="a35a1-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a35a1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a35a1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a35a1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a35a1-106">Imposta o restituisce il testo visualizzato per [**l'oggetto Command**](/windows/desktop/lwef/the-command-object) nella finestra Comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="a35a1-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="a35a1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a35a1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a35a1-108">*agent.\***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). Stringa_ \*  \[  =  *VoiceCaption*\]</span><span class="sxs-lookup"><span data-stu-id="a35a1-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="a35a1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a35a1-109">Part</span></span>     | <span data-ttu-id="a35a1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a35a1-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="a35a1-111">*string*</span><span class="sxs-lookup"><span data-stu-id="a35a1-111">*string*</span></span> | <span data-ttu-id="a35a1-112">Espressione stringa che restituisce il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a35a1-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a35a1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a35a1-113">Remarks</span></span>

<span data-ttu-id="a35a1-114">Se si definisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una raccolta [**Commands**](https://www.bing.com/search?q=**Commands**) e si imposta la relativa [**proprietà Voice,**](voice-property.md) in genere si imposta anche la [**relativa proprietà VoiceCaption.**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a35a1-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="a35a1-115">Questo testo verrà visualizzato nella finestra Comandi vocali quando l'applicazione client è attiva per l'input e il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="a35a1-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="a35a1-116">Se questa proprietà non è impostata, l'impostazione della [**proprietà Caption**](caption-property.md) determina il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a35a1-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="a35a1-117">Quando la proprietà **VoiceCaption** e **Caption** non è impostata, il comando non viene visualizzato nella finestra Comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="a35a1-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="a35a1-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a35a1-118">See Also</span></span>

[<span data-ttu-id="a35a1-119">**Caption - proprietà**</span><span class="sxs-lookup"><span data-stu-id="a35a1-119">**Caption property**</span></span>](caption-property.md)


 

 
