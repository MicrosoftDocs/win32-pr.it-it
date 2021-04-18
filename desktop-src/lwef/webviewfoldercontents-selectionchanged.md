---
title: Evento WebViewFolderContents. SelectionChanged (shldisp. h)
description: Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Funzionalità dell'ambiente Windows legacy dell'evento SelectionChanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518748"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="bb438-104">Evento WebViewFolderContents. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="bb438-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="bb438-105">Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bb438-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb438-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb438-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="bb438-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb438-107">Parameters</span></span>

<span data-ttu-id="bb438-108">Questo gestore eventi non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="bb438-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="bb438-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="bb438-109">Examples</span></span>

<span data-ttu-id="bb438-110">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo evento per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="bb438-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="bb438-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb438-111">Requirements</span></span>



| <span data-ttu-id="bb438-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb438-112">Requirement</span></span> | <span data-ttu-id="bb438-113">Valore</span><span class="sxs-lookup"><span data-stu-id="bb438-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb438-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb438-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bb438-115">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb438-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bb438-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb438-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bb438-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb438-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb438-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb438-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb438-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb438-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bb438-120">IDL</span><span class="sxs-lookup"><span data-stu-id="bb438-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb438-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb438-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bb438-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bb438-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb438-123"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bb438-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





