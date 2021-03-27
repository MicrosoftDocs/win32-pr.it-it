---
description: Indica che lo stato di selezione di uno o più elementi nella vista è stato modificato.
title: Evento ShellFolderViewOC. SelectionChanged (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347921"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="113a9-103">Evento ShellFolderViewOC. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="113a9-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="113a9-104">Indica che lo stato di selezione di uno o più elementi nella vista è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="113a9-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="113a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="113a9-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="113a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="113a9-106">Parameters</span></span>

<span data-ttu-id="113a9-107">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="113a9-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="113a9-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="113a9-108">Remarks</span></span>

<span data-ttu-id="113a9-109">Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="113a9-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="113a9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113a9-110">Requirements</span></span>



| <span data-ttu-id="113a9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="113a9-111">Requirement</span></span> | <span data-ttu-id="113a9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="113a9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="113a9-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113a9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="113a9-114">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="113a9-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="113a9-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113a9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="113a9-116">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="113a9-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="113a9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="113a9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="113a9-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="113a9-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="113a9-119">IDL</span><span class="sxs-lookup"><span data-stu-id="113a9-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="113a9-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="113a9-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="113a9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="113a9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="113a9-122"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="113a9-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="113a9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113a9-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="113a9-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




