---
title: Oggetto Command
description: Oggetto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299698"
---
# <a name="the-command-object"></a><span data-ttu-id="9859e-103">Oggetto Command</span><span class="sxs-lookup"><span data-stu-id="9859e-103">The Command Object</span></span>

<span data-ttu-id="9859e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9859e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9859e-105">Un oggetto [**Command**](/windows/desktop/lwef/the-command-object) è un elemento in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="9859e-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="9859e-106">Il server consente all'utente di accedere agli oggetti **Command** quando l'applicazione client diventa attiva.</span><span class="sxs-lookup"><span data-stu-id="9859e-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="9859e-107">Proprietà oggetto comando</span><span class="sxs-lookup"><span data-stu-id="9859e-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="9859e-108">Per accedere alla proprietà di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) , è possibile farvi riferimento nella relativa raccolta usando la relativa proprietà [**Name**](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9859e-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="9859e-109">In VBScript e Visual Basic è possibile usare direttamente la proprietà **Name** :</span><span class="sxs-lookup"><span data-stu-id="9859e-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="9859e-110">Per i linguaggi di programmazione che non supportano le raccolte, usare il metodo di [**comando**](command-method.md) :</span><span class="sxs-lookup"><span data-stu-id="9859e-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="9859e-111">È anche possibile fare riferimento a un oggetto comando creando un riferimento a esso.</span><span class="sxs-lookup"><span data-stu-id="9859e-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="9859e-112">In Visual Basic dichiarare una variabile oggetto e utilizzare l'istruzione set per creare il riferimento:</span><span class="sxs-lookup"><span data-stu-id="9859e-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="9859e-113">In Visual Basic 5,0, è anche possibile dichiarare l'oggetto come tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e creare il riferimento.</span><span class="sxs-lookup"><span data-stu-id="9859e-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="9859e-114">Questa convenzione Abilita il binding anticipato, con conseguente miglioramento delle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="9859e-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="9859e-115">In VBScript è possibile dichiarare un riferimento come un particolare tipo, ma è comunque possibile dichiarare la variabile e impostarla sul [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta:</span><span class="sxs-lookup"><span data-stu-id="9859e-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="9859e-116">Un comando può essere visualizzato nel menu di scelta rapida del carattere e nella finestra comandi oppure in entrambi.</span><span class="sxs-lookup"><span data-stu-id="9859e-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="9859e-117">Per visualizzare nel menu a comparsa, deve avere una didascalia e impostare la proprietà [**Visible**](visible-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="9859e-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="9859e-118">Inoltre, la proprietà **Visible** dell'oggetto raccolta Commands deve essere impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="9859e-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="9859e-119">Per visualizzare nella finestra dei comandi, è necessario impostare le proprietà [**Caption**](caption-property.md) e [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="9859e-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="9859e-120">Si noti che le voci di menu popup di un carattere non cambiano mentre il menu viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9859e-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="9859e-121">Se si aggiungono o si rimuovono i comandi o se ne modificano le proprietà quando viene visualizzato il menu popup del carattere, il menu Visualizza tali modifiche ogni volta che l'utente lo Visualizza.</span><span class="sxs-lookup"><span data-stu-id="9859e-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="9859e-122">Tuttavia, la finestra comandi riflette in modo dinamico tutte le modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="9859e-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="9859e-123">Nella tabella seguente viene riepilogato il modo in cui le proprietà di un [**comando**](/windows/desktop/lwef/the-command-object) influiscono sulla presentazione:</span><span class="sxs-lookup"><span data-stu-id="9859e-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="9859e-124">Proprietà Caption</span><span class="sxs-lookup"><span data-stu-id="9859e-124">Caption Property</span></span>

<span data-ttu-id="9859e-125">Proprietà Voice-Caption</span><span class="sxs-lookup"><span data-stu-id="9859e-125">Voice-Caption Property</span></span>

<span data-ttu-id="9859e-126">Proprietà Voice</span><span class="sxs-lookup"><span data-stu-id="9859e-126">Voice Property</span></span>

<span data-ttu-id="9859e-127">Visible (proprietà)</span><span class="sxs-lookup"><span data-stu-id="9859e-127">Visible Property</span></span>

<span data-ttu-id="9859e-128">Proprietà Enabled</span><span class="sxs-lookup"><span data-stu-id="9859e-128">Enabled Property</span></span>

<span data-ttu-id="9859e-129">Viene visualizzato nel menu a comparsa del carattere</span><span class="sxs-lookup"><span data-stu-id="9859e-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="9859e-130">Viene visualizzato nella finestra comandi</span><span class="sxs-lookup"><span data-stu-id="9859e-130">Appears in Commands Window</span></span>

<span data-ttu-id="9859e-131">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-131">Yes</span></span>

<span data-ttu-id="9859e-132">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-132">Yes</span></span>

<span data-ttu-id="9859e-133">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-133">Yes</span></span>

<span data-ttu-id="9859e-134">True</span><span class="sxs-lookup"><span data-stu-id="9859e-134">True</span></span>

<span data-ttu-id="9859e-135">True</span><span class="sxs-lookup"><span data-stu-id="9859e-135">True</span></span>

<span data-ttu-id="9859e-136">Normale, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-137">Sì, uso di [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="9859e-138">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-138">Yes</span></span>

<span data-ttu-id="9859e-139">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-139">Yes</span></span>

<span data-ttu-id="9859e-140">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-140">Yes</span></span>

<span data-ttu-id="9859e-141">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-141">True</span></span>

<span data-ttu-id="9859e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-142">False</span></span>

<span data-ttu-id="9859e-143">Disabilitato, utilizzo della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-144">No</span><span class="sxs-lookup"><span data-stu-id="9859e-144">No</span></span>

<span data-ttu-id="9859e-145">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-145">Yes</span></span>

<span data-ttu-id="9859e-146">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-146">Yes</span></span>

<span data-ttu-id="9859e-147">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-147">Yes</span></span>

<span data-ttu-id="9859e-148">False</span><span class="sxs-lookup"><span data-stu-id="9859e-148">False</span></span>

<span data-ttu-id="9859e-149">True</span><span class="sxs-lookup"><span data-stu-id="9859e-149">True</span></span>

<span data-ttu-id="9859e-150">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-150">Does not appear</span></span>

<span data-ttu-id="9859e-151">Sì, uso di [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="9859e-152">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-152">Yes</span></span>

<span data-ttu-id="9859e-153">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-153">Yes</span></span>

<span data-ttu-id="9859e-154">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-154">Yes</span></span>

<span data-ttu-id="9859e-155">False</span><span class="sxs-lookup"><span data-stu-id="9859e-155">False</span></span>

<span data-ttu-id="9859e-156">False</span><span class="sxs-lookup"><span data-stu-id="9859e-156">False</span></span>

<span data-ttu-id="9859e-157">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-157">Does not appear</span></span>

<span data-ttu-id="9859e-158">No</span><span class="sxs-lookup"><span data-stu-id="9859e-158">No</span></span>

<span data-ttu-id="9859e-159">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-159">Yes</span></span>

<span data-ttu-id="9859e-160">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-160">Yes</span></span>

<span data-ttu-id="9859e-161">No</span><span class="sxs-lookup"><span data-stu-id="9859e-161">No</span></span> 

<span data-ttu-id="9859e-162">True</span><span class="sxs-lookup"><span data-stu-id="9859e-162">True</span></span>

<span data-ttu-id="9859e-163">True</span><span class="sxs-lookup"><span data-stu-id="9859e-163">True</span></span>

<span data-ttu-id="9859e-164">Normale, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-165">No</span><span class="sxs-lookup"><span data-stu-id="9859e-165">No</span></span>

<span data-ttu-id="9859e-166">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-166">Yes</span></span>

<span data-ttu-id="9859e-167">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-167">Yes</span></span>

<span data-ttu-id="9859e-168">No</span><span class="sxs-lookup"><span data-stu-id="9859e-168">No</span></span> 

<span data-ttu-id="9859e-169">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-169">True</span></span>

<span data-ttu-id="9859e-170">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-170">False</span></span>

<span data-ttu-id="9859e-171">Disabilitato, utilizzo della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-172">No</span><span class="sxs-lookup"><span data-stu-id="9859e-172">No</span></span>

<span data-ttu-id="9859e-173">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-173">Yes</span></span>

<span data-ttu-id="9859e-174">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-174">Yes</span></span>

<span data-ttu-id="9859e-175">No</span><span class="sxs-lookup"><span data-stu-id="9859e-175">No</span></span> 

<span data-ttu-id="9859e-176">False</span><span class="sxs-lookup"><span data-stu-id="9859e-176">False</span></span>

<span data-ttu-id="9859e-177">True</span><span class="sxs-lookup"><span data-stu-id="9859e-177">True</span></span>

<span data-ttu-id="9859e-178">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-178">Does not appear</span></span>

<span data-ttu-id="9859e-179">No</span><span class="sxs-lookup"><span data-stu-id="9859e-179">No</span></span>

<span data-ttu-id="9859e-180">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-180">Yes</span></span>

<span data-ttu-id="9859e-181">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-181">Yes</span></span>

<span data-ttu-id="9859e-182">No</span><span class="sxs-lookup"><span data-stu-id="9859e-182">No</span></span> 

<span data-ttu-id="9859e-183">False</span><span class="sxs-lookup"><span data-stu-id="9859e-183">False</span></span>

<span data-ttu-id="9859e-184">False</span><span class="sxs-lookup"><span data-stu-id="9859e-184">False</span></span>

<span data-ttu-id="9859e-185">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-185">Does not appear</span></span>

<span data-ttu-id="9859e-186">No</span><span class="sxs-lookup"><span data-stu-id="9859e-186">No</span></span>

<span data-ttu-id="9859e-187">No</span><span class="sxs-lookup"><span data-stu-id="9859e-187">No</span></span> 

<span data-ttu-id="9859e-188">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-188">Yes</span></span>

<span data-ttu-id="9859e-189">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-189">Yes</span></span>

<span data-ttu-id="9859e-190">True</span><span class="sxs-lookup"><span data-stu-id="9859e-190">True</span></span>

<span data-ttu-id="9859e-191">True</span><span class="sxs-lookup"><span data-stu-id="9859e-191">True</span></span>

<span data-ttu-id="9859e-192">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-192">Does not appear</span></span>

<span data-ttu-id="9859e-193">Sì, uso di [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="9859e-194">No</span><span class="sxs-lookup"><span data-stu-id="9859e-194">No</span></span> 

<span data-ttu-id="9859e-195">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-195">Yes</span></span>

<span data-ttu-id="9859e-196">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-196">Yes</span></span>

<span data-ttu-id="9859e-197">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-197">True</span></span>

<span data-ttu-id="9859e-198">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-198">False</span></span>

<span data-ttu-id="9859e-199">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-199">Does not appear</span></span>

<span data-ttu-id="9859e-200">No</span><span class="sxs-lookup"><span data-stu-id="9859e-200">No</span></span>

<span data-ttu-id="9859e-201">No</span><span class="sxs-lookup"><span data-stu-id="9859e-201">No</span></span> 

<span data-ttu-id="9859e-202">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-202">Yes</span></span>

<span data-ttu-id="9859e-203">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-203">Yes</span></span>

<span data-ttu-id="9859e-204">False</span><span class="sxs-lookup"><span data-stu-id="9859e-204">False</span></span>

<span data-ttu-id="9859e-205">True</span><span class="sxs-lookup"><span data-stu-id="9859e-205">True</span></span>

<span data-ttu-id="9859e-206">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-206">Does not appear</span></span>

<span data-ttu-id="9859e-207">Sì, uso di [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="9859e-208">No</span><span class="sxs-lookup"><span data-stu-id="9859e-208">No</span></span> 

<span data-ttu-id="9859e-209">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-209">Yes</span></span>

<span data-ttu-id="9859e-210">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-210">Yes</span></span>

<span data-ttu-id="9859e-211">False</span><span class="sxs-lookup"><span data-stu-id="9859e-211">False</span></span>

<span data-ttu-id="9859e-212">False</span><span class="sxs-lookup"><span data-stu-id="9859e-212">False</span></span>

<span data-ttu-id="9859e-213">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-213">Does not appear</span></span>

<span data-ttu-id="9859e-214">No</span><span class="sxs-lookup"><span data-stu-id="9859e-214">No</span></span>

<span data-ttu-id="9859e-215">No</span><span class="sxs-lookup"><span data-stu-id="9859e-215">No</span></span> 

<span data-ttu-id="9859e-216">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-216">Yes</span></span>

<span data-ttu-id="9859e-217">No</span><span class="sxs-lookup"><span data-stu-id="9859e-217">No</span></span> 

<span data-ttu-id="9859e-218">True</span><span class="sxs-lookup"><span data-stu-id="9859e-218">True</span></span>

<span data-ttu-id="9859e-219">True</span><span class="sxs-lookup"><span data-stu-id="9859e-219">True</span></span>

<span data-ttu-id="9859e-220">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-220">Does not appear</span></span>

<span data-ttu-id="9859e-221">No</span><span class="sxs-lookup"><span data-stu-id="9859e-221">No</span></span>

<span data-ttu-id="9859e-222">No</span><span class="sxs-lookup"><span data-stu-id="9859e-222">No</span></span> 

<span data-ttu-id="9859e-223">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-223">Yes</span></span>

<span data-ttu-id="9859e-224">No</span><span class="sxs-lookup"><span data-stu-id="9859e-224">No</span></span> 

<span data-ttu-id="9859e-225">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-225">True</span></span>

<span data-ttu-id="9859e-226">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-226">False</span></span>

<span data-ttu-id="9859e-227">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-227">Does not appear</span></span>

<span data-ttu-id="9859e-228">No</span><span class="sxs-lookup"><span data-stu-id="9859e-228">No</span></span>

<span data-ttu-id="9859e-229">No</span><span class="sxs-lookup"><span data-stu-id="9859e-229">No</span></span> 

<span data-ttu-id="9859e-230">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-230">Yes</span></span>

<span data-ttu-id="9859e-231">No</span><span class="sxs-lookup"><span data-stu-id="9859e-231">No</span></span> 

<span data-ttu-id="9859e-232">False</span><span class="sxs-lookup"><span data-stu-id="9859e-232">False</span></span>

<span data-ttu-id="9859e-233">True</span><span class="sxs-lookup"><span data-stu-id="9859e-233">True</span></span>

<span data-ttu-id="9859e-234">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-234">Does not appear</span></span>

<span data-ttu-id="9859e-235">No</span><span class="sxs-lookup"><span data-stu-id="9859e-235">No</span></span>

<span data-ttu-id="9859e-236">No</span><span class="sxs-lookup"><span data-stu-id="9859e-236">No</span></span> 

<span data-ttu-id="9859e-237">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-237">Yes</span></span>

<span data-ttu-id="9859e-238">No</span><span class="sxs-lookup"><span data-stu-id="9859e-238">No</span></span> 

<span data-ttu-id="9859e-239">False</span><span class="sxs-lookup"><span data-stu-id="9859e-239">False</span></span>

<span data-ttu-id="9859e-240">False</span><span class="sxs-lookup"><span data-stu-id="9859e-240">False</span></span>

<span data-ttu-id="9859e-241">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-241">Does not appear</span></span>

<span data-ttu-id="9859e-242">No</span><span class="sxs-lookup"><span data-stu-id="9859e-242">No</span></span>

<span data-ttu-id="9859e-243">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-243">Yes</span></span>

<span data-ttu-id="9859e-244">No</span><span class="sxs-lookup"><span data-stu-id="9859e-244">No</span></span> 

<span data-ttu-id="9859e-245">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-245">Yes</span></span>

<span data-ttu-id="9859e-246">True</span><span class="sxs-lookup"><span data-stu-id="9859e-246">True</span></span>

<span data-ttu-id="9859e-247">True</span><span class="sxs-lookup"><span data-stu-id="9859e-247">True</span></span>

<span data-ttu-id="9859e-248">Normale, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-249">Sì, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-250">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-250">Yes</span></span>

<span data-ttu-id="9859e-251">No</span><span class="sxs-lookup"><span data-stu-id="9859e-251">No</span></span> 

<span data-ttu-id="9859e-252">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-252">Yes</span></span>

<span data-ttu-id="9859e-253">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-253">True</span></span>

<span data-ttu-id="9859e-254">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-254">False</span></span>

<span data-ttu-id="9859e-255">Disabilitato, utilizzo della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-256">No</span><span class="sxs-lookup"><span data-stu-id="9859e-256">No</span></span>

<span data-ttu-id="9859e-257">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-257">Yes</span></span>

<span data-ttu-id="9859e-258">No</span><span class="sxs-lookup"><span data-stu-id="9859e-258">No</span></span> 

<span data-ttu-id="9859e-259">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-259">Yes</span></span>

<span data-ttu-id="9859e-260">False</span><span class="sxs-lookup"><span data-stu-id="9859e-260">False</span></span>

<span data-ttu-id="9859e-261">True</span><span class="sxs-lookup"><span data-stu-id="9859e-261">True</span></span>

<span data-ttu-id="9859e-262">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-262">Does not appear</span></span>

<span data-ttu-id="9859e-263">Sì, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-264">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-264">Yes</span></span>

<span data-ttu-id="9859e-265">No</span><span class="sxs-lookup"><span data-stu-id="9859e-265">No</span></span> 

<span data-ttu-id="9859e-266">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-266">Yes</span></span>

<span data-ttu-id="9859e-267">False</span><span class="sxs-lookup"><span data-stu-id="9859e-267">False</span></span>

<span data-ttu-id="9859e-268">False</span><span class="sxs-lookup"><span data-stu-id="9859e-268">False</span></span>

<span data-ttu-id="9859e-269">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-269">Does not appear</span></span>

<span data-ttu-id="9859e-270">No</span><span class="sxs-lookup"><span data-stu-id="9859e-270">No</span></span>

<span data-ttu-id="9859e-271">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-271">Yes</span></span>

<span data-ttu-id="9859e-272">No</span><span class="sxs-lookup"><span data-stu-id="9859e-272">No</span></span> 

<span data-ttu-id="9859e-273">No</span><span class="sxs-lookup"><span data-stu-id="9859e-273">No</span></span> 

<span data-ttu-id="9859e-274">True</span><span class="sxs-lookup"><span data-stu-id="9859e-274">True</span></span>

<span data-ttu-id="9859e-275">True</span><span class="sxs-lookup"><span data-stu-id="9859e-275">True</span></span>

<span data-ttu-id="9859e-276">Normale, uso della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-277">No</span><span class="sxs-lookup"><span data-stu-id="9859e-277">No</span></span>

<span data-ttu-id="9859e-278">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-278">Yes</span></span>

<span data-ttu-id="9859e-279">No</span><span class="sxs-lookup"><span data-stu-id="9859e-279">No</span></span> 

<span data-ttu-id="9859e-280">No</span><span class="sxs-lookup"><span data-stu-id="9859e-280">No</span></span> 

<span data-ttu-id="9859e-281">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-281">True</span></span>

<span data-ttu-id="9859e-282">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-282">False</span></span>

<span data-ttu-id="9859e-283">Disabilitato, utilizzo della [ **didascalia**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="9859e-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="9859e-284">No</span><span class="sxs-lookup"><span data-stu-id="9859e-284">No</span></span>

<span data-ttu-id="9859e-285">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-285">Yes</span></span>

<span data-ttu-id="9859e-286">No</span><span class="sxs-lookup"><span data-stu-id="9859e-286">No</span></span> 

<span data-ttu-id="9859e-287">No</span><span class="sxs-lookup"><span data-stu-id="9859e-287">No</span></span> 

<span data-ttu-id="9859e-288">False</span><span class="sxs-lookup"><span data-stu-id="9859e-288">False</span></span>

<span data-ttu-id="9859e-289">True</span><span class="sxs-lookup"><span data-stu-id="9859e-289">True</span></span>

<span data-ttu-id="9859e-290">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-290">Does not appear</span></span>

<span data-ttu-id="9859e-291">No</span><span class="sxs-lookup"><span data-stu-id="9859e-291">No</span></span>

<span data-ttu-id="9859e-292">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-292">Yes</span></span>

<span data-ttu-id="9859e-293">No</span><span class="sxs-lookup"><span data-stu-id="9859e-293">No</span></span> 

<span data-ttu-id="9859e-294">No</span><span class="sxs-lookup"><span data-stu-id="9859e-294">No</span></span> 

<span data-ttu-id="9859e-295">False</span><span class="sxs-lookup"><span data-stu-id="9859e-295">False</span></span>

<span data-ttu-id="9859e-296">False</span><span class="sxs-lookup"><span data-stu-id="9859e-296">False</span></span>

<span data-ttu-id="9859e-297">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-297">Does not appear</span></span>

<span data-ttu-id="9859e-298">No</span><span class="sxs-lookup"><span data-stu-id="9859e-298">No</span></span>

<span data-ttu-id="9859e-299">No</span><span class="sxs-lookup"><span data-stu-id="9859e-299">No</span></span> 

<span data-ttu-id="9859e-300">No</span><span class="sxs-lookup"><span data-stu-id="9859e-300">No</span></span> 

<span data-ttu-id="9859e-301">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-301">Yes</span></span>

<span data-ttu-id="9859e-302">True</span><span class="sxs-lookup"><span data-stu-id="9859e-302">True</span></span>

<span data-ttu-id="9859e-303">True</span><span class="sxs-lookup"><span data-stu-id="9859e-303">True</span></span>

<span data-ttu-id="9859e-304">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-304">Does not appear</span></span>

<span data-ttu-id="9859e-305">No</span><span class="sxs-lookup"><span data-stu-id="9859e-305">No</span></span> 

<span data-ttu-id="9859e-306">No</span><span class="sxs-lookup"><span data-stu-id="9859e-306">No</span></span> 

<span data-ttu-id="9859e-307">No</span><span class="sxs-lookup"><span data-stu-id="9859e-307">No</span></span> 

<span data-ttu-id="9859e-308">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-308">Yes</span></span>

<span data-ttu-id="9859e-309">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-309">True</span></span>

<span data-ttu-id="9859e-310">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-310">False</span></span>

<span data-ttu-id="9859e-311">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-311">Does not appear</span></span>

<span data-ttu-id="9859e-312">No</span><span class="sxs-lookup"><span data-stu-id="9859e-312">No</span></span>

<span data-ttu-id="9859e-313">No</span><span class="sxs-lookup"><span data-stu-id="9859e-313">No</span></span> 

<span data-ttu-id="9859e-314">No</span><span class="sxs-lookup"><span data-stu-id="9859e-314">No</span></span> 

<span data-ttu-id="9859e-315">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-315">Yes</span></span>

<span data-ttu-id="9859e-316">False</span><span class="sxs-lookup"><span data-stu-id="9859e-316">False</span></span>

<span data-ttu-id="9859e-317">True</span><span class="sxs-lookup"><span data-stu-id="9859e-317">True</span></span>

<span data-ttu-id="9859e-318">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-318">Does not appear</span></span>

<span data-ttu-id="9859e-319">No</span><span class="sxs-lookup"><span data-stu-id="9859e-319">No</span></span> 

<span data-ttu-id="9859e-320">No</span><span class="sxs-lookup"><span data-stu-id="9859e-320">No</span></span> 

<span data-ttu-id="9859e-321">No</span><span class="sxs-lookup"><span data-stu-id="9859e-321">No</span></span> 

<span data-ttu-id="9859e-322">Sì</span><span class="sxs-lookup"><span data-stu-id="9859e-322">Yes</span></span>

<span data-ttu-id="9859e-323">False</span><span class="sxs-lookup"><span data-stu-id="9859e-323">False</span></span>

<span data-ttu-id="9859e-324">False</span><span class="sxs-lookup"><span data-stu-id="9859e-324">False</span></span>

<span data-ttu-id="9859e-325">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-325">Does not appear</span></span>

<span data-ttu-id="9859e-326">No</span><span class="sxs-lookup"><span data-stu-id="9859e-326">No</span></span>

<span data-ttu-id="9859e-327">No</span><span class="sxs-lookup"><span data-stu-id="9859e-327">No</span></span> 

<span data-ttu-id="9859e-328">No</span><span class="sxs-lookup"><span data-stu-id="9859e-328">No</span></span> 

<span data-ttu-id="9859e-329">No</span><span class="sxs-lookup"><span data-stu-id="9859e-329">No</span></span> 

<span data-ttu-id="9859e-330">True</span><span class="sxs-lookup"><span data-stu-id="9859e-330">True</span></span>

<span data-ttu-id="9859e-331">True</span><span class="sxs-lookup"><span data-stu-id="9859e-331">True</span></span>

<span data-ttu-id="9859e-332">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-332">Does not appear</span></span>

<span data-ttu-id="9859e-333">No</span><span class="sxs-lookup"><span data-stu-id="9859e-333">No</span></span>

<span data-ttu-id="9859e-334">No</span><span class="sxs-lookup"><span data-stu-id="9859e-334">No</span></span> 

<span data-ttu-id="9859e-335">No</span><span class="sxs-lookup"><span data-stu-id="9859e-335">No</span></span> 

<span data-ttu-id="9859e-336">No</span><span class="sxs-lookup"><span data-stu-id="9859e-336">No</span></span> 

<span data-ttu-id="9859e-337">Vero</span><span class="sxs-lookup"><span data-stu-id="9859e-337">True</span></span>

<span data-ttu-id="9859e-338">Falso</span><span class="sxs-lookup"><span data-stu-id="9859e-338">False</span></span>

<span data-ttu-id="9859e-339">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-339">Does not appear</span></span>

<span data-ttu-id="9859e-340">No</span><span class="sxs-lookup"><span data-stu-id="9859e-340">No</span></span>

<span data-ttu-id="9859e-341">No</span><span class="sxs-lookup"><span data-stu-id="9859e-341">No</span></span> 

<span data-ttu-id="9859e-342">No</span><span class="sxs-lookup"><span data-stu-id="9859e-342">No</span></span> 

<span data-ttu-id="9859e-343">No</span><span class="sxs-lookup"><span data-stu-id="9859e-343">No</span></span> 

<span data-ttu-id="9859e-344">False</span><span class="sxs-lookup"><span data-stu-id="9859e-344">False</span></span>

<span data-ttu-id="9859e-345">True</span><span class="sxs-lookup"><span data-stu-id="9859e-345">True</span></span>

<span data-ttu-id="9859e-346">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-346">Does not appear</span></span>

<span data-ttu-id="9859e-347">No</span><span class="sxs-lookup"><span data-stu-id="9859e-347">No</span></span>

<span data-ttu-id="9859e-348">No</span><span class="sxs-lookup"><span data-stu-id="9859e-348">No</span></span> 

<span data-ttu-id="9859e-349">No</span><span class="sxs-lookup"><span data-stu-id="9859e-349">No</span></span> 

<span data-ttu-id="9859e-350">No</span><span class="sxs-lookup"><span data-stu-id="9859e-350">No</span></span> 

<span data-ttu-id="9859e-351">False</span><span class="sxs-lookup"><span data-stu-id="9859e-351">False</span></span>

<span data-ttu-id="9859e-352">False</span><span class="sxs-lookup"><span data-stu-id="9859e-352">False</span></span>

<span data-ttu-id="9859e-353">Non viene visualizzato</span><span class="sxs-lookup"><span data-stu-id="9859e-353">Does not appear</span></span>

<span data-ttu-id="9859e-354">No</span><span class="sxs-lookup"><span data-stu-id="9859e-354">No</span></span>

 <span data-ttu-id="9859e-355">Se l'impostazione della proprietà è null.</span><span class="sxs-lookup"><span data-stu-id="9859e-355">If the property setting is null.</span></span> <span data-ttu-id="9859e-356">In alcuni linguaggi di programmazione è possibile che una stringa vuota non venga interpretata come una stringa null.</span><span class="sxs-lookup"><span data-stu-id="9859e-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="9859e-357">Il comando è ancora accessibile tramite voce.</span><span class="sxs-lookup"><span data-stu-id="9859e-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="9859e-358">Quando il server riceve l'input per uno dei comandi, invia un evento di [**comando**](/windows/desktop/lwef/the-command-object) e passa di nuovo il nome del **comando** come attributo dell'oggetto [**userinput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="9859e-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="9859e-359">È quindi possibile usare le istruzioni condizionali per trovare una corrispondenza ed elaborare il **comando**.</span><span class="sxs-lookup"><span data-stu-id="9859e-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

