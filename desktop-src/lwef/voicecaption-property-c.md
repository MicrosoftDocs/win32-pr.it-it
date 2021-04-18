---
title: Proprietà VoiceCaption (oggetto Command)
description: Proprietà VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300819"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="c7553-103">Proprietà VoiceCaption (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="c7553-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="c7553-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7553-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c7553-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c7553-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c7553-106">Imposta o restituisce il testo visualizzato per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="c7553-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="c7553-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="c7553-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c7553-108">\*Agent. \***Characters ("**_CharacterID_*_"). Comandi ("_*_Name_\*_")._ \*  \[  =  *Stringa* VoiceCaption\]</span><span class="sxs-lookup"><span data-stu-id="c7553-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="c7553-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c7553-109">Part</span></span>     | <span data-ttu-id="c7553-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7553-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="c7553-111">*string*</span><span class="sxs-lookup"><span data-stu-id="c7553-111">*string*</span></span> | <span data-ttu-id="c7553-112">Espressione stringa che restituisce il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c7553-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7553-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7553-113">Remarks</span></span>

<span data-ttu-id="c7553-114">Se si definisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](https://www.bing.com/search?q=**Commands**) e si imposta la relativa proprietà [**Voice**](voice-property.md) , in genere viene impostata anche la relativa proprietà [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c7553-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="c7553-115">Questo testo verrà visualizzato nella finestra comandi vocali quando l'applicazione client è di input-attivo e il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="c7553-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="c7553-116">Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) determina il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c7553-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="c7553-117">Quando non viene impostata la proprietà **VoiceCaption** né **Caption** , il comando non viene visualizzato nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="c7553-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="c7553-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c7553-118">See Also</span></span>

[<span data-ttu-id="c7553-119">**Proprietà Caption**</span><span class="sxs-lookup"><span data-stu-id="c7553-119">**Caption property**</span></span>](caption-property.md)


 

 
