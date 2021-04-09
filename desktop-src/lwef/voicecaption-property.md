---
title: Proprietà VoiceCaption (oggetto Commands)
description: Proprietà VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739479"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="10b66-103">Proprietà VoiceCaption (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="10b66-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="10b66-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10b66-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="10b66-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="10b66-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="10b66-106">Restituisce o imposta il testo visualizzato per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="10b66-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="10b66-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="10b66-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="10b66-108">\*Agent. \***Characters ("**_CharacterID_\*_"). Stringa Commands. VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="10b66-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="10b66-109">Parte</span><span class="sxs-lookup"><span data-stu-id="10b66-109">Part</span></span>     | <span data-ttu-id="10b66-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b66-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="10b66-111">*string*</span><span class="sxs-lookup"><span data-stu-id="10b66-111">*string*</span></span> | <span data-ttu-id="10b66-112">Espressione stringa che restituisce il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="10b66-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10b66-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="10b66-113">Remarks</span></span>

<span data-ttu-id="10b66-114">Se si imposta la proprietà [**Voice**](voice-property.md) della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , in genere si imposta anche la relativa proprietà **VoiceCaption** .</span><span class="sxs-lookup"><span data-stu-id="10b66-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="10b66-115">L'impostazione di testo **VoiceCaption** viene visualizzata nella finestra comandi vocali quando l'applicazione client è di tipo input-attivo e il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="10b66-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="10b66-116">Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) della raccolta di **comandi** determina il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="10b66-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="10b66-117">Quando non viene impostata la proprietà **VoiceCaption** o **Caption** , i comandi della raccolta vengono visualizzati nella finestra comandi vocali in "(comando undefined)" quando l'applicazione client diventa input-Active.</span><span class="sxs-lookup"><span data-stu-id="10b66-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="10b66-118">L'impostazione **VoiceCaption** determina anche il testo visualizzato nel suggerimento di ascolto per indicare i comandi per i quali il carattere è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="10b66-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="10b66-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="10b66-119">See Also</span></span>

[<span data-ttu-id="10b66-120">Proprietà Caption</span><span class="sxs-lookup"><span data-stu-id="10b66-120">Caption property</span></span>](caption-property.md)


 

 
