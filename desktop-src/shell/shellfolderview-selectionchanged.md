---
description: Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.
title: Evento ShellFolderView. SelectionChanged (shldisp. h)
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
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: 864cd4c7bb0b414e4237c698412ad10899c8cbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058120"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="e8a59-103">Evento ShellFolderView. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="e8a59-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="e8a59-104">Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8a59-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a59-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8a59-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="e8a59-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8a59-106">Parameters</span></span>

<span data-ttu-id="e8a59-107">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="e8a59-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a59-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8a59-108">Requirements</span></span>



| <span data-ttu-id="e8a59-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a59-109">Requirement</span></span> | <span data-ttu-id="e8a59-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e8a59-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a59-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a59-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a59-112">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8a59-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e8a59-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a59-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a59-114">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8a59-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8a59-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8a59-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a59-116"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a59-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e8a59-117">IDL</span><span class="sxs-lookup"><span data-stu-id="e8a59-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8a59-118"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8a59-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e8a59-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a59-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a59-120"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a59-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




