---
title: Proprietà filelima
description: Proprietà filelima
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710921"
---
# <a name="helpfile-property"></a><span data-ttu-id="65a9c-103">Proprietà filelima</span><span class="sxs-lookup"><span data-stu-id="65a9c-103">HelpFile Property</span></span>

<span data-ttu-id="65a9c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65a9c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="65a9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="65a9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="65a9c-106">Restituisce o imposta il percorso e il nome file di un file della Guida sensibile al contesto di Microsoft Windows fornito dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="65a9c-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="65a9c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="65a9c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="65a9c-108">\*agente. ***Caratteri ("*** CharacterID \* \* *").* \*  \[  =  *Nome file* fileguida\]</span><span class="sxs-lookup"><span data-stu-id="65a9c-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="65a9c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="65a9c-109">Part</span></span>       | <span data-ttu-id="65a9c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65a9c-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="65a9c-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="65a9c-111">*Filename*</span></span> | <span data-ttu-id="65a9c-112">Espressione stringa che specifica il percorso e il nome del file della Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="65a9c-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65a9c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="65a9c-113">Remarks</span></span>

<span data-ttu-id="65a9c-114">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata **la proprietà filecommand del carattere** , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere o seleziona un comando dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="65a9c-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="65a9c-115">Se nella proprietà [**HelpContextID**](helpcontextid-property.md) del comando selezionato è stato specificato un numero di contesto, nella Guida viene visualizzato un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".</span><span class="sxs-lookup"><span data-stu-id="65a9c-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="65a9c-116">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="65a9c-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="65a9c-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="65a9c-117">See Also</span></span>

<span data-ttu-id="65a9c-118">[**Proprietà HelpModeOn**](helpmodeon-property.md), [ **proprietà HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="65a9c-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




