---
description: Indica che l'oggetto ShellFolderView ha terminato l'enumerazione del contenuto della cartella.
title: Evento ShellFolderViewOC. EnumDone (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994989"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="1b023-103">Evento ShellFolderViewOC. EnumDone</span><span class="sxs-lookup"><span data-stu-id="1b023-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="1b023-104">Indica che l'oggetto [**ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="1b023-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b023-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b023-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="1b023-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b023-106">Parameters</span></span>

<span data-ttu-id="1b023-107">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="1b023-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b023-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b023-108">Remarks</span></span>

<span data-ttu-id="1b023-109">L'oggetto [**ShellFolderView**](shellfolderview.md) deve enumerare il contenuto di una cartella prima di poterlo visualizzare.</span><span class="sxs-lookup"><span data-stu-id="1b023-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="1b023-110">Con le cartelle di grandi dimensioni o che si trovano in un sistema remoto, questo processo può richiedere fino a diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="1b023-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="1b023-111">Durante questo periodo, viene visualizzata un'immagine di torcia elettrica animata che indica all'utente che l'elaborazione è in corso.</span><span class="sxs-lookup"><span data-stu-id="1b023-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="1b023-112">Al termine dell'enumerazione, viene generato l'evento **EnumDone** e il grafico della torcia viene sostituito dal contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="1b023-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="1b023-113">Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1b023-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="1b023-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b023-114">Requirements</span></span>



| <span data-ttu-id="1b023-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b023-115">Requirement</span></span> | <span data-ttu-id="1b023-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1b023-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b023-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b023-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b023-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b023-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b023-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b023-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b023-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b023-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1b023-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b023-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b023-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b023-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1b023-123">IDL</span><span class="sxs-lookup"><span data-stu-id="1b023-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b023-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b023-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1b023-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1b023-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b023-126"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1b023-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b023-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b023-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b023-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="1b023-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




