---
title: Proprietà HelpContextID (oggetto Command)
description: Proprietà HelpContextID
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118859"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="b9508-103">Proprietà HelpContextID (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="b9508-103">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="b9508-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9508-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b9508-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b9508-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b9508-106">Restituisce o imposta un numero di contesto associato per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="b9508-106">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="b9508-107">Utilizzato per fornire la Guida sensibile al contesto per l'oggetto **Command** .</span><span class="sxs-lookup"><span data-stu-id="b9508-107">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="b9508-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b9508-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b9508-109">\*Agent. \***Characters ("**_CharacterID_\*_"). Comandi ("")._ \*  \[  =  *Numero* HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="b9508-109">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="b9508-110">Parte</span><span class="sxs-lookup"><span data-stu-id="b9508-110">Part</span></span>     | <span data-ttu-id="b9508-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9508-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="b9508-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="b9508-112">*Number*</span></span> | <span data-ttu-id="b9508-113">Integer che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="b9508-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9508-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9508-114">Remarks</span></span>

<span data-ttu-id="b9508-115">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata [**la proprietà filecommand del carattere**](helpfile-property.md) sul file, Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il comando.</span><span class="sxs-lookup"><span data-stu-id="b9508-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="b9508-116">Se si imposta un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="b9508-116">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="b9508-117">Il numero di contesto corrente è il valore di **HelpContextID** per il comando.</span><span class="sxs-lookup"><span data-stu-id="b9508-117">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="b9508-118">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="b9508-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="b9508-119">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b9508-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b9508-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9508-120">See Also</span></span>

[<span data-ttu-id="b9508-121">**Proprietà filelima**</span><span class="sxs-lookup"><span data-stu-id="b9508-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
