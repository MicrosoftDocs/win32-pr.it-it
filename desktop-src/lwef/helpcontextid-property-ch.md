---
title: Proprietà HelpContextID (oggetto characters)
description: Proprietà HelpContextID
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400108"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="12da5-103">Proprietà HelpContextID (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="12da5-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="12da5-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12da5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="12da5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="12da5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="12da5-106">Restituisce o imposta un numero di contesto associato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="12da5-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="12da5-107">Utilizzato per fornire la Guida sensibile al contesto per il carattere.</span><span class="sxs-lookup"><span data-stu-id="12da5-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="12da5-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="12da5-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="12da5-109">\*Agent. \***Characters ("**_CharacterID_\*_")._ \*  \[  =  *Numero* HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="12da5-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="12da5-110">Parte</span><span class="sxs-lookup"><span data-stu-id="12da5-110">Part</span></span>     | <span data-ttu-id="12da5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12da5-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="12da5-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="12da5-112">*Number*</span></span> | <span data-ttu-id="12da5-113">Integer che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="12da5-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12da5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="12da5-114">Remarks</span></span>

<span data-ttu-id="12da5-115">Per supportare la Guida sensibile al contesto per il carattere, assegnare il numero di contesto al carattere usato per l'argomento della Guida associato quando si compila il file della guida.</span><span class="sxs-lookup"><span data-stu-id="12da5-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="12da5-116">Questa proprietà si applica solo al client del carattere; l'impostazione non influisce sugli altri client del carattere o di altri caratteri del client.</span><span class="sxs-lookup"><span data-stu-id="12da5-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="12da5-117">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata [**la proprietà fileitem del carattere**](helpfile-property.md) , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere.</span><span class="sxs-lookup"><span data-stu-id="12da5-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="12da5-118">Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="12da5-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="12da5-119">Il numero di contesto corrente è il valore di **HelpContextID** per il carattere.</span><span class="sxs-lookup"><span data-stu-id="12da5-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="12da5-120">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="12da5-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="12da5-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="12da5-121">See Also</span></span>

[<span data-ttu-id="12da5-122">**Proprietà filelima**</span><span class="sxs-lookup"><span data-stu-id="12da5-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




