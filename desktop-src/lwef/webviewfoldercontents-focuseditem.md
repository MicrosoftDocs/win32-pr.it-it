---
title: Proprietà WebViewFolderContents. FocusedItem (shldisp. h)
description: Ottiene un oggetto FolderItem che rappresenta l'elemento con lo stato attivo per l'input.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà FocusedItem
- Proprietà FocusedItem ambiente Windows legacy funzionalità, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400266"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="4280a-106">Proprietà WebViewFolderContents. FocusedItem</span><span class="sxs-lookup"><span data-stu-id="4280a-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="4280a-107">Ottiene un oggetto [**FolderItem**](../shell/folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="4280a-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="4280a-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4280a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4280a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4280a-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="4280a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4280a-110">Property value</span></span>

<span data-ttu-id="4280a-111">Variabile di tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto elemento con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4280a-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="4280a-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="4280a-112">Examples</span></span>

<span data-ttu-id="4280a-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="4280a-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



## <a name="requirements"></a><span data-ttu-id="4280a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4280a-114">Requirements</span></span>



| <span data-ttu-id="4280a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4280a-115">Requirement</span></span> | <span data-ttu-id="4280a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4280a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4280a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4280a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4280a-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4280a-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4280a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4280a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4280a-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4280a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4280a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4280a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4280a-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4280a-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4280a-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4280a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4280a-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4280a-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4280a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4280a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4280a-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4280a-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

