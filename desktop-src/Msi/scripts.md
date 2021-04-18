---
description: Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312315"
---
# <a name="scripts"></a><span data-ttu-id="25f13-103">Script</span><span class="sxs-lookup"><span data-stu-id="25f13-103">Scripts</span></span>

<span data-ttu-id="25f13-104">Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="25f13-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="25f13-105">Windows Installer non fornisce il modulo di gestione di script.</span><span class="sxs-lookup"><span data-stu-id="25f13-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="25f13-106">Gli autori che desiderano utilizzare un linguaggio di scripting durante l'installazione devono pertanto garantire che sia disponibile il motore di scripting appropriato.</span><span class="sxs-lookup"><span data-stu-id="25f13-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="25f13-107">Il programma di installazione non supporta la versione JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="25f13-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="25f13-108">Un'azione personalizzata a 64 bit basata sugli script deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico azioni personalizzate nella colonna Type della tabella [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25f13-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="25f13-109">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="25f13-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="25f13-110">I tipi di azione personalizzati di base seguenti chiamano funzioni scritte nello script.</span><span class="sxs-lookup"><span data-stu-id="25f13-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="25f13-111">Tipo di azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="25f13-111">Custom action type</span></span>                                 | <span data-ttu-id="25f13-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25f13-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25f13-113">Tipo di azione personalizzata 5</span><span class="sxs-lookup"><span data-stu-id="25f13-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="25f13-114">File JScript archiviato in un flusso di tabella binario.</span><span class="sxs-lookup"><span data-stu-id="25f13-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="25f13-115">Tipo di azione personalizzata 21</span><span class="sxs-lookup"><span data-stu-id="25f13-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="25f13-116">File JScript installato con un prodotto.</span><span class="sxs-lookup"><span data-stu-id="25f13-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="25f13-117">Tipo di azione personalizzata 53</span><span class="sxs-lookup"><span data-stu-id="25f13-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="25f13-118">Testo JScript specificato da un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="25f13-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="25f13-119">Tipo di azione personalizzata 37</span><span class="sxs-lookup"><span data-stu-id="25f13-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="25f13-120">Testo JScript archiviato nella colonna di destinazione della tabella [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25f13-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="25f13-121">Tipo di azione personalizzata 6</span><span class="sxs-lookup"><span data-stu-id="25f13-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="25f13-122">File VBScript archiviato in un flusso di tabella [binario](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25f13-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="25f13-123">Tipo di azione personalizzata 22</span><span class="sxs-lookup"><span data-stu-id="25f13-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="25f13-124">File VBScript installato con un prodotto.</span><span class="sxs-lookup"><span data-stu-id="25f13-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="25f13-125">Tipo di azione personalizzata 54</span><span class="sxs-lookup"><span data-stu-id="25f13-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="25f13-126">Testo VBScript specificato da un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="25f13-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="25f13-127">Tipo di azione personalizzata 38</span><span class="sxs-lookup"><span data-stu-id="25f13-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="25f13-128">Testo VBScript archiviato nella colonna di destinazione della tabella [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25f13-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="25f13-129">Il programma di installazione esegue azioni personalizzate script direttamente e non usa Windows script host.</span><span class="sxs-lookup"><span data-stu-id="25f13-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="25f13-130">Impossibile utilizzare l'oggetto **WScript** all'interno di un'azione personalizzata script perché questo oggetto viene fornito da Windows script host.</span><span class="sxs-lookup"><span data-stu-id="25f13-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="25f13-131">Gli oggetti nel modello a oggetti di Windows script host possono essere utilizzati solo in azioni personalizzate se Windows script host è installato nel computer creando nuove istanze dell'oggetto, con una chiamata a CreateObject e specificando il ProgId dell'oggetto, ad esempio "WScript. Shell".</span><span class="sxs-lookup"><span data-stu-id="25f13-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="25f13-132">A seconda del tipo di azione personalizzata script, l'accesso ad alcuni oggetti e metodi del modello a oggetti di Windows script host può essere negato per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="25f13-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="25f13-133">Per ulteriori informazioni, vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un riepilogo di tutti i tipi di azioni personalizzate e la relativa modalità di codifica nella tabella [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25f13-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



