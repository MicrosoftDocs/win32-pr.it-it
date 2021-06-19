---
title: Proprietà VoiceCaption (oggetto Commands)
description: Informazioni sulla proprietà VoiceCaption dell'oggetto Commands, che restituisce o imposta il testo visualizzato per l'oggetto Commands nella finestra Comandi vocali.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396126"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="cde23-103">Proprietà VoiceCaption (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="cde23-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="cde23-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cde23-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cde23-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cde23-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cde23-106">Restituisce o imposta il testo visualizzato per [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) nella finestra Comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="cde23-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="cde23-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="cde23-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cde23-108">*agent.\***Characters("**_CharacterID_*_"). Stringa Commands.VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="cde23-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="cde23-109">Parte</span><span class="sxs-lookup"><span data-stu-id="cde23-109">Part</span></span>     | <span data-ttu-id="cde23-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cde23-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="cde23-111">*string*</span><span class="sxs-lookup"><span data-stu-id="cde23-111">*string*</span></span> | <span data-ttu-id="cde23-112">Espressione stringa che restituisce il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="cde23-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cde23-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cde23-113">Remarks</span></span>

<span data-ttu-id="cde23-114">Se si imposta la [**proprietà Voice**](voice-property.md) della raccolta [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) in genere si imposta anche la **relativa proprietà VoiceCaption.**</span><span class="sxs-lookup"><span data-stu-id="cde23-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="cde23-115">**L'impostazione di testo VoiceCaption** viene visualizzata nella finestra Comandi vocali quando l'applicazione client è attiva per l'input e il carattere è visibile.</span><span class="sxs-lookup"><span data-stu-id="cde23-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="cde23-116">Se questa proprietà non è impostata, l'impostazione della proprietà [**Caption**](caption-property.md) della raccolta **Commands** determina il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="cde23-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="cde23-117">Quando nessuna delle due proprietà **VoiceCaption** o **Caption** è impostata, i comandi nella raccolta vengono visualizzati nella finestra Comandi vocali in "(comando non definito)" quando l'applicazione client diventa attiva per l'input.</span><span class="sxs-lookup"><span data-stu-id="cde23-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="cde23-118">**L'impostazione VoiceCaption** determina anche il testo visualizzato nel suggerimento di ascolto per indicare i comandi per cui il carattere è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="cde23-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="cde23-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cde23-119">See Also</span></span>

[<span data-ttu-id="cde23-120">Proprietà Caption</span><span class="sxs-lookup"><span data-stu-id="cde23-120">Caption property</span></span>](caption-property.md)


 

 
