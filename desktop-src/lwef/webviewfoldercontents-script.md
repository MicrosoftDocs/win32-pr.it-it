---
title: Proprietà WebViewFolderContents. script (shldisp. h)
description: Ottiene l'oggetto di scripting per la visualizzazione.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Proprietà script per le funzionalità dell'ambiente Windows legacy
- Proprietà script funzionalità ambiente Windows legacy, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302379"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="f21aa-106">Proprietà WebViewFolderContents. script</span><span class="sxs-lookup"><span data-stu-id="f21aa-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="f21aa-107">Ottiene l'oggetto di scripting per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f21aa-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="f21aa-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f21aa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21aa-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f21aa-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="f21aa-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f21aa-110">Property value</span></span>

<span data-ttu-id="f21aa-111">Variabile di tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto di scripting.</span><span class="sxs-lookup"><span data-stu-id="f21aa-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="f21aa-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="f21aa-112">Examples</span></span>

<span data-ttu-id="f21aa-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="f21aa-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="f21aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f21aa-114">Requirements</span></span>



| <span data-ttu-id="f21aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21aa-115">Requirement</span></span> | <span data-ttu-id="f21aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f21aa-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21aa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f21aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f21aa-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f21aa-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f21aa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f21aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f21aa-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f21aa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f21aa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f21aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f21aa-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21aa-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f21aa-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f21aa-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f21aa-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f21aa-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f21aa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f21aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f21aa-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f21aa-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

