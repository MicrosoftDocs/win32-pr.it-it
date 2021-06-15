---
title: Proprietà HelpContextID (oggetto raccolta Commands)
description: Informazioni sulla proprietà HelpContextID dell'oggetto raccolta Commands. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068237"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="75cbb-104">Proprietà HelpContextID (oggetto raccolta Commands)</span><span class="sxs-lookup"><span data-stu-id="75cbb-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="75cbb-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75cbb-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="75cbb-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="75cbb-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="75cbb-107">Restituisce o imposta un numero di contesto associato per [**l'oggetto**](/windows/desktop/lwef/the-commands-collection-object) Commands.</span><span class="sxs-lookup"><span data-stu-id="75cbb-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="75cbb-108">Usato per fornire la Guida sensibile al contesto per **l'oggetto** Commands.</span><span class="sxs-lookup"><span data-stu-id="75cbb-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="75cbb-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="75cbb-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="75cbb-110">*agent.\***Characters("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID_ \*  \[  =  *Number*\]</span><span class="sxs-lookup"><span data-stu-id="75cbb-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="75cbb-111">Parte</span><span class="sxs-lookup"><span data-stu-id="75cbb-111">Part</span></span>     | <span data-ttu-id="75cbb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75cbb-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="75cbb-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="75cbb-113">*Number*</span></span> | <span data-ttu-id="75cbb-114">Intero che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="75cbb-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75cbb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="75cbb-115">Remarks</span></span>

<span data-ttu-id="75cbb-116">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Agent chiama automaticamente help quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona l'oggetto [**Commands.**](/windows/desktop/lwef/the-commands-collection-object)</span><span class="sxs-lookup"><span data-stu-id="75cbb-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="75cbb-117">Se si imposta un numero di contesto in **HelpContextID**, Agent chiama la Guida e cerca l'argomento identificato da tale numero di contesto.</span><span class="sxs-lookup"><span data-stu-id="75cbb-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="75cbb-118">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="75cbb-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="75cbb-119">La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75cbb-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="75cbb-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="75cbb-120">See Also</span></span>

[<span data-ttu-id="75cbb-121">**Proprietà HelpFile**</span><span class="sxs-lookup"><span data-stu-id="75cbb-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
