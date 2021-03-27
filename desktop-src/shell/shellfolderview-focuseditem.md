---
description: Ottiene un oggetto FolderItem che rappresenta l'elemento con lo stato attivo per l'input.
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Proprietà ShellFolderView. FocusedItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26f0f24cddd3b9299ec70b41160579659c71b5bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233201"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="8c15a-103">Proprietà ShellFolderView. FocusedItem</span><span class="sxs-lookup"><span data-stu-id="8c15a-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="8c15a-104">Ottiene un oggetto [**FolderItem**](folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="8c15a-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="8c15a-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8c15a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c15a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c15a-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="8c15a-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8c15a-107">Property value</span></span>

<span data-ttu-id="8c15a-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto elemento con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="8c15a-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c15a-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c15a-109">Remarks</span></span>

<span data-ttu-id="8c15a-110">**FocusedItem** può essere chiamato solo sul sistema locale.</span><span class="sxs-lookup"><span data-stu-id="8c15a-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="8c15a-111">Non funzionerà se eseguita in una pagina Web su HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="8c15a-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="8c15a-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c15a-112">Examples</span></span>

<span data-ttu-id="8c15a-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="8c15a-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="8c15a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c15a-114">Requirements</span></span>



| <span data-ttu-id="8c15a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c15a-115">Requirement</span></span> | <span data-ttu-id="8c15a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c15a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c15a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c15a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c15a-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8c15a-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c15a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c15a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c15a-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c15a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c15a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c15a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c15a-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c15a-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8c15a-123">IDL</span><span class="sxs-lookup"><span data-stu-id="8c15a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c15a-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c15a-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8c15a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c15a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c15a-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8c15a-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
