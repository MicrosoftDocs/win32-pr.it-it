---
title: Proprietà HelpContextID (oggetto Collection Commands)
description: Proprietà HelpContextID
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474921"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="a4434-103">Proprietà HelpContextID (oggetto Collection Commands)</span><span class="sxs-lookup"><span data-stu-id="a4434-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="a4434-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4434-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a4434-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a4434-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a4434-106">Restituisce o imposta un numero di contesto associato per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="a4434-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="a4434-107">Utilizzato per fornire la Guida sensibile al contesto per l'oggetto **Commands** .</span><span class="sxs-lookup"><span data-stu-id="a4434-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="a4434-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a4434-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a4434-109">\*Agent. \***Characters ("**_CharacterID_*_"). Comandi ("_*_Name_\*_")._ \*  \[  =  *Numero* HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="a4434-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="a4434-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a4434-110">Part</span></span>     | <span data-ttu-id="a4434-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4434-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="a4434-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="a4434-112">*Number*</span></span> | <span data-ttu-id="a4434-113">Integer che specifica un numero di contesto valido.</span><span class="sxs-lookup"><span data-stu-id="a4434-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4434-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4434-114">Remarks</span></span>

<span data-ttu-id="a4434-115">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà filecommand [**del carattere**](helpfile-property.md) , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="a4434-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="a4434-116">Se si imposta un numero di contesto in **HelpContextID**, Agent chiama la guida e cerca l'argomento identificato da tale numero di contesto.</span><span class="sxs-lookup"><span data-stu-id="a4434-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="a4434-117">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a4434-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="a4434-118">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4434-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a4434-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a4434-119">See Also</span></span>

[<span data-ttu-id="a4434-120">**Proprietà filelima**</span><span class="sxs-lookup"><span data-stu-id="a4434-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
