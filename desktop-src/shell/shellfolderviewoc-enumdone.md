---
description: Indica che l'oggetto ShellFolderView ha terminato l'enumerazione del contenuto della cartella.
title: Evento ShellFolderViewOC.EnumDone (Shldisp.h)
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
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841052"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="8c4a7-103">Evento ShellFolderViewOC.EnumDone</span><span class="sxs-lookup"><span data-stu-id="8c4a7-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="8c4a7-104">Indica che [**l'oggetto ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c4a7-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="8c4a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c4a7-106">Parameters</span></span>

<span data-ttu-id="8c4a7-107">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c4a7-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c4a7-108">Remarks</span></span>

<span data-ttu-id="8c4a7-109">[**L'oggetto ShellFolderView**](shellfolderview.md) deve enumerare il contenuto di una cartella prima di poterla visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="8c4a7-110">Con le cartelle di grandi dimensioni o che si trovano in un sistema remoto, questo processo può richiedere fino a diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="8c4a7-111">Durante questo periodo, viene visualizzata una torcia animata per indicare all'utente che è in corso l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="8c4a7-112">Al termine dell'enumerazione, viene generato l'evento **EnumDone** e il grafico torcia viene sostituito dal contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="8c4a7-113">Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8c4a7-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="8c4a7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c4a7-114">Requirements</span></span>



| <span data-ttu-id="8c4a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4a7-115">Requirement</span></span> | <span data-ttu-id="8c4a7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c4a7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4a7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c4a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c4a7-118">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8c4a7-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c4a7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c4a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c4a7-120">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c4a7-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8c4a7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c4a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c4a7-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4a7-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8c4a7-123">Idl</span><span class="sxs-lookup"><span data-stu-id="8c4a7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c4a7-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c4a7-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8c4a7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c4a7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c4a7-126"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8c4a7-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4a7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c4a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4a7-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="8c4a7-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




