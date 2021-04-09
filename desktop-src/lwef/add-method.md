---
title: Aggiungi metodo
description: Aggiungi metodo
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044602"
---
# <a name="add-method"></a><span data-ttu-id="62092-103">Aggiungi metodo</span><span class="sxs-lookup"><span data-stu-id="62092-103">Add Method</span></span>

<span data-ttu-id="62092-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62092-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="62092-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="62092-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="62092-106">Aggiunge un oggetto [Command](the-command-object.md) alla raccolta di [comandi](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="62092-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="62092-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="62092-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Comandi. aggiungere* il \*  *nome*, la *didascalia*, la *voce*, *abilitata*, *visibile*</span><span class="sxs-lookup"><span data-stu-id="62092-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="62092-109">Parte</span><span class="sxs-lookup"><span data-stu-id="62092-109">Part</span></span>      | <span data-ttu-id="62092-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62092-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62092-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="62092-111">*Name*</span></span>    | <span data-ttu-id="62092-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="62092-112">Required.</span></span> <span data-ttu-id="62092-113">Valore stringa corrispondente all'ID assegnato per il comando.</span><span class="sxs-lookup"><span data-stu-id="62092-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="62092-114">*Didascalia*</span><span class="sxs-lookup"><span data-stu-id="62092-114">*Caption*</span></span> | <span data-ttu-id="62092-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62092-115">Optional.</span></span> <span data-ttu-id="62092-116">Valore stringa corrispondente al nome che verrà visualizzato nel menu di scelta rapida del carattere e nella finestra comandi quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="62092-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="62092-117">Per ulteriori informazioni, vedere la proprietà [Caption](caption-property.md) dell'oggetto [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="62092-118">*Chiamata vocale*</span><span class="sxs-lookup"><span data-stu-id="62092-118">*Voice*</span></span>   | <span data-ttu-id="62092-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62092-119">Optional.</span></span> <span data-ttu-id="62092-120">Valore stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di riconoscimento vocale per il riconoscimento di questo comando.</span><span class="sxs-lookup"><span data-stu-id="62092-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="62092-121">Per ulteriori informazioni sulla formattazione di alternative per la stringa, vedere la proprietà [Voice](voice-property.md) dell'oggetto [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="62092-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="62092-122">*Enabled*</span></span> | <span data-ttu-id="62092-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62092-123">Optional.</span></span> <span data-ttu-id="62092-124">Valore booleano che indica se il comando è abilitato.</span><span class="sxs-lookup"><span data-stu-id="62092-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="62092-125">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="62092-125">The default value is **True**.</span></span> <span data-ttu-id="62092-126">Per ulteriori informazioni, vedere la proprietà [Enabled](enabled-property.md) dell'oggetto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="62092-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="62092-127">*Visible*</span></span> | <span data-ttu-id="62092-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62092-128">Optional.</span></span> <span data-ttu-id="62092-129">Valore booleano che indica se il comando è visibile nel menu popup del carattere per il carattere quando l'applicazione client è di tipo input-attivo.</span><span class="sxs-lookup"><span data-stu-id="62092-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="62092-130">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="62092-130">The default value is **True**.</span></span> <span data-ttu-id="62092-131">Per ulteriori informazioni, vedere la proprietà [Visible](visible-property.md) dell'oggetto [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62092-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="62092-132">Remarks</span></span>

<span data-ttu-id="62092-133">Il valore della proprietà [Name](name-property.md) di un oggetto [Command](the-command-object.md) deve essere univoco all'interno della relativa raccolta di [comandi](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="62092-134">Prima di poter creare un nuovo comando con la stessa impostazione della proprietà Name, è necessario rimuovere un comando.</span><span class="sxs-lookup"><span data-stu-id="62092-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="62092-135">Il tentativo di creare un comando con una proprietà Name già esistente genera un errore.</span><span class="sxs-lookup"><span data-stu-id="62092-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="62092-136">Questo metodo restituisce anche un oggetto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="62092-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="62092-137">In questo modo è possibile dichiarare un oggetto e assegnarvi un comando quando si chiama addMethod.</span><span class="sxs-lookup"><span data-stu-id="62092-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="62092-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62092-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62092-139">**Insert (metodo)**</span><span class="sxs-lookup"><span data-stu-id="62092-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="62092-140">**RemoveAll, metodo**</span><span class="sxs-lookup"><span data-stu-id="62092-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="62092-141">**Remove (metodo)**</span><span class="sxs-lookup"><span data-stu-id="62092-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




