---
title: Proprietà HelpContextID (oggetto Command)
description: Informazioni sulla proprietà HelpContextID dell'oggetto Command. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068513"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="1f412-104">Proprietà HelpContextID (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="1f412-104">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="1f412-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f412-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1f412-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1f412-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1f412-107">Restituisce o imposta un numero di contesto associato per [**l'oggetto**](/windows/desktop/lwef/the-command-object) Command.</span><span class="sxs-lookup"><span data-stu-id="1f412-107">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="1f412-108">Usato per fornire la Guida sensibile al contesto per **l'oggetto** Command.</span><span class="sxs-lookup"><span data-stu-id="1f412-108">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="1f412-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="1f412-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1f412-110">*agent.\***Characters("**_CharacterID_*_"). Commands(""). Numero_ \*  \[  =  *HelpContextID*\]</span><span class="sxs-lookup"><span data-stu-id="1f412-110">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="1f412-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1f412-111">Part</span></span>     | <span data-ttu-id="1f412-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f412-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="1f412-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="1f412-113">*Number*</span></span> | <span data-ttu-id="1f412-114">Intero che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="1f412-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f412-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f412-115">Remarks</span></span>

<span data-ttu-id="1f412-116">Se è stato creato un file della Guida di Windows per l'applicazione e si imposta la proprietà [**HelpFile**](helpfile-property.md) del carattere sul file, Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona il comando.</span><span class="sxs-lookup"><span data-stu-id="1f412-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="1f412-117">Se si imposta un numero di contesto in [**HelpContextID,**](helpcontextid-property.md)Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="1f412-117">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="1f412-118">Il numero di contesto corrente è il valore **di HelpContextID** per il comando.</span><span class="sxs-lookup"><span data-stu-id="1f412-118">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="1f412-119">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="1f412-119">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="1f412-120">La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1f412-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1f412-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1f412-121">See Also</span></span>

[<span data-ttu-id="1f412-122">**Proprietà HelpFile**</span><span class="sxs-lookup"><span data-stu-id="1f412-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 
