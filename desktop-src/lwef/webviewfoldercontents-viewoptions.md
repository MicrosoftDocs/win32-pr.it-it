---
title: Proprietà WebViewFolderContents. ViewOptions (shldisp. h)
description: Ottiene un set di flag ShellFolderViewOptions che indicano le opzioni correnti della visualizzazione.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà ViewOptions
- Proprietà ViewOptions ambiente Windows legacy funzionalità, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047950"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="93777-106">Proprietà WebViewFolderContents. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="93777-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="93777-107">Ottiene un set di flag [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) che indicano le opzioni correnti della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="93777-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="93777-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="93777-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93777-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93777-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="93777-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="93777-110">Property value</span></span>

<span data-ttu-id="93777-111">Variabile di tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto opzioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="93777-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="93777-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="93777-112">Examples</span></span>

<span data-ttu-id="93777-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="93777-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="93777-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93777-114">Requirements</span></span>



| <span data-ttu-id="93777-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="93777-115">Requirement</span></span> | <span data-ttu-id="93777-116">Valore</span><span class="sxs-lookup"><span data-stu-id="93777-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93777-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93777-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93777-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93777-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="93777-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93777-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93777-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93777-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93777-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93777-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="93777-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93777-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="93777-123">IDL</span><span class="sxs-lookup"><span data-stu-id="93777-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93777-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93777-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="93777-125">DLL</span><span class="sxs-lookup"><span data-stu-id="93777-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93777-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="93777-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

