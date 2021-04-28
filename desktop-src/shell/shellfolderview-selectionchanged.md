---
description: 'Evento ShellFolderView.SelectionChanged: si verifica quando viene modificato lo stato di selezione di uno o più elementi nella visualizzazione.'
title: Evento ShellFolderView.SelectionChanged (Shldisp.h)
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
ms.openlocfilehash: 31a32865a979bf6b5fa115912bdc32a9680e5064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103999"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="a65b8-103">Evento ShellFolderView.SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="a65b8-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="a65b8-104">Si verifica quando lo stato di selezione di uno o più elementi nella visualizzazione viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a65b8-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a65b8-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="a65b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a65b8-106">Parameters</span></span>

<span data-ttu-id="a65b8-107">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a65b8-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a65b8-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a65b8-108">Requirements</span></span>



| <span data-ttu-id="a65b8-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65b8-109">Requirement</span></span> | <span data-ttu-id="a65b8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a65b8-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65b8-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65b8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a65b8-112">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a65b8-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a65b8-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65b8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a65b8-114">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a65b8-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a65b8-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a65b8-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65b8-116"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a65b8-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a65b8-117">Idl</span><span class="sxs-lookup"><span data-stu-id="a65b8-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a65b8-118"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a65b8-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a65b8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a65b8-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65b8-120"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a65b8-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




