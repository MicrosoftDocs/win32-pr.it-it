---
description: 'Proprietà ShellFolderView.Folder: ottiene un oggetto Folder che rappresenta la visualizzazione.'
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Proprietà ShellFolderView.Folder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083419"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="0c0f5-103">ShellFolderView.Folder - proprietà</span><span class="sxs-lookup"><span data-stu-id="0c0f5-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="0c0f5-104">Ottiene un [**oggetto Folder**](folder.md) che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c0f5-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="0c0f5-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0c0f5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0f5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c0f5-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="0c0f5-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0c0f5-107">Property value</span></span>

<span data-ttu-id="0c0f5-108">Oggetto che riceve [**l'oggetto Folder.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="0c0f5-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c0f5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c0f5-109">Remarks</span></span>

<span data-ttu-id="0c0f5-110">**La** cartella può essere chiamata solo nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="0c0f5-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="0c0f5-111">Non funzionerà quando viene eseguito in una pagina Web tramite HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="0c0f5-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="0c0f5-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="0c0f5-112">Examples</span></span>

<span data-ttu-id="0c0f5-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="0c0f5-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="0c0f5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c0f5-114">Requirements</span></span>



| <span data-ttu-id="0c0f5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c0f5-115">Requirement</span></span> | <span data-ttu-id="0c0f5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c0f5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0f5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c0f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0f5-118">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0c0f5-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c0f5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c0f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0f5-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0c0f5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c0f5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c0f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c0f5-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c0f5-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0c0f5-123">Idl</span><span class="sxs-lookup"><span data-stu-id="0c0f5-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c0f5-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c0f5-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0c0f5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c0f5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c0f5-126"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0c0f5-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




