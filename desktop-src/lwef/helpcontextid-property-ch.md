---
title: Proprietà HelpContextID (oggetto Characters)
description: Informazioni sulla proprietà HelpContextID dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068187"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="59d93-104">Proprietà HelpContextID (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="59d93-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="59d93-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59d93-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="59d93-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="59d93-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="59d93-107">Restituisce o imposta un numero di contesto associato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="59d93-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="59d93-108">Utilizzato per fornire la Guida sensibile al contesto per il carattere.</span><span class="sxs-lookup"><span data-stu-id="59d93-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="59d93-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="59d93-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="59d93-110">*agent.\***Characters("**_CharacterID_*_"). HelpContextID_ \*  \[  =  *Number*\]</span><span class="sxs-lookup"><span data-stu-id="59d93-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="59d93-111">Parte</span><span class="sxs-lookup"><span data-stu-id="59d93-111">Part</span></span>     | <span data-ttu-id="59d93-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59d93-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="59d93-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="59d93-113">*Number*</span></span> | <span data-ttu-id="59d93-114">Intero che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="59d93-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59d93-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="59d93-115">Remarks</span></span>

<span data-ttu-id="59d93-116">Per supportare la Guida sensibile al contesto per il carattere, assegnare il numero di contesto al carattere utilizzato per l'argomento della Guida associato quando si compila il file della Guida.</span><span class="sxs-lookup"><span data-stu-id="59d93-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="59d93-117">Questa proprietà si applica solo al client del carattere. L'impostazione non influisce sugli altri client del carattere o di altri caratteri del client.</span><span class="sxs-lookup"><span data-stu-id="59d93-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="59d93-118">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Agent chiama automaticamente help quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente fa clic sul carattere.</span><span class="sxs-lookup"><span data-stu-id="59d93-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="59d93-119">Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="59d93-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="59d93-120">Il numero di contesto corrente è il valore **di HelpContextID** per il carattere.</span><span class="sxs-lookup"><span data-stu-id="59d93-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="59d93-121">La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="59d93-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="59d93-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="59d93-122">See Also</span></span>

[<span data-ttu-id="59d93-123">**Proprietà HelpFile**</span><span class="sxs-lookup"><span data-stu-id="59d93-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




