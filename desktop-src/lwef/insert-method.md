---
title: Insert (metodo)
description: Insert (metodo)
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299768"
---
# <a name="insert-method"></a><span data-ttu-id="a198d-103">Insert (metodo)</span><span class="sxs-lookup"><span data-stu-id="a198d-103">Insert Method</span></span>

<span data-ttu-id="a198d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a198d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a198d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a198d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a198d-106">Inserisce un oggetto **Command** nell'insieme **Commands** .</span><span class="sxs-lookup"><span data-stu-id="a198d-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="a198d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a198d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a198d-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Commands. Insert* \*  *Name*, *refname*, *before*\_</span><span class="sxs-lookup"><span data-stu-id="a198d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="a198d-109">*Didascalia*, *voce, abilitata, visibile*</span><span class="sxs-lookup"><span data-stu-id="a198d-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="a198d-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a198d-110">Part</span></span>      | <span data-ttu-id="a198d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a198d-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a198d-112">*Nome*</span><span class="sxs-lookup"><span data-stu-id="a198d-112">*Name*</span></span>    | <span data-ttu-id="a198d-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a198d-113">Required.</span></span> <span data-ttu-id="a198d-114">Valore stringa corrispondente all'ID assegnato al [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="a198d-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a198d-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="a198d-115">*RefName*</span></span> | <span data-ttu-id="a198d-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a198d-116">Required.</span></span> <span data-ttu-id="a198d-117">Valore stringa corrispondente al nome (ID) del comando appena sopra o al di sotto del quale si desidera inserire il nuovo comando.</span><span class="sxs-lookup"><span data-stu-id="a198d-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="a198d-118">*Prima*</span><span class="sxs-lookup"><span data-stu-id="a198d-118">*Before*</span></span>  | <span data-ttu-id="a198d-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a198d-119">Optional.</span></span> <span data-ttu-id="a198d-120">Valore booleano che indica se inserire il nuovo comando prima del comando specificato da *refname*.</span><span class="sxs-lookup"><span data-stu-id="a198d-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="a198d-121">**True** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a198d-121">**True** (Default).</span></span> <span data-ttu-id="a198d-122">Il nuovo comando verrà inserito prima del comando a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="a198d-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="a198d-123">**False** Il nuovo comando verrà inserito dopo il comando a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="a198d-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="a198d-124">*Didascalia*</span><span class="sxs-lookup"><span data-stu-id="a198d-124">*Caption*</span></span> | <span data-ttu-id="a198d-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a198d-125">Optional.</span></span> <span data-ttu-id="a198d-126">Valore stringa corrispondente al nome che verrà visualizzato nel menu di scelta rapida del carattere e nella finestra comandi quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="a198d-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="a198d-127">Per ulteriori informazioni, vedere la proprietà [**Caption**](caption-property.md)dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="a198d-128">*Chiamata vocale*</span><span class="sxs-lookup"><span data-stu-id="a198d-128">*Voice*</span></span>   | <span data-ttu-id="a198d-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a198d-129">Optional.</span></span> <span data-ttu-id="a198d-130">Valore stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di riconoscimento vocale per il riconoscimento di questo comando.</span><span class="sxs-lookup"><span data-stu-id="a198d-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="a198d-131">Per ulteriori informazioni sulla formattazione di alternative per la stringa, vedere la proprietà **Voice** dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="a198d-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="a198d-132">*Enabled*</span></span> | <span data-ttu-id="a198d-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a198d-133">Optional.</span></span> <span data-ttu-id="a198d-134">Valore booleano che indica se il comando è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a198d-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="a198d-135">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="a198d-135">The default value is **True**.</span></span> <span data-ttu-id="a198d-136">Per ulteriori informazioni, vedere la proprietà **Enabled** dell'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="a198d-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="a198d-137">*Visible*</span></span> | <span data-ttu-id="a198d-138">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a198d-138">Optional.</span></span> <span data-ttu-id="a198d-139">Valore booleano che indica se il comando è visibile nella finestra dei comandi quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="a198d-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="a198d-140">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="a198d-140">The default value is **True**.</span></span> <span data-ttu-id="a198d-141">Per ulteriori informazioni, vedere la proprietà [**Visible**](visible-property.md) dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a198d-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="a198d-142">Remarks</span></span>

<span data-ttu-id="a198d-143">Il valore della proprietà [**Name**](name-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) deve essere univoco all'interno della relativa raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="a198d-144">Prima di poter creare un nuovo **comando** con la stessa impostazione della proprietà **Name** , è necessario rimuovere un **comando** .</span><span class="sxs-lookup"><span data-stu-id="a198d-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="a198d-145">Il tentativo di creare un **comando** con una proprietà **Name** già esistente genera un errore.</span><span class="sxs-lookup"><span data-stu-id="a198d-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="a198d-146">Questo metodo restituisce anche un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a198d-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="a198d-147">In questo modo è possibile dichiarare un oggetto e assegnarvi un **comando** quando si chiama il metodo **Insert** .</span><span class="sxs-lookup"><span data-stu-id="a198d-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="a198d-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a198d-148">See Also</span></span>

<span data-ttu-id="a198d-149">Metodo [**Add**](add-method.md), [**Remove**](remove-method.md), metodo [**RemoveAll**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="a198d-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

