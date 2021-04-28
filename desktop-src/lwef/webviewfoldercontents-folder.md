---
title: Proprietà WebViewFolderContents.Folder (Shldisp.h)
description: 'Proprietà WebViewFolderContents.Folder: ottiene un oggetto Folder che rappresenta la visualizzazione.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Proprietà Cartella Funzionalità dell'ambiente Windows legacy
- Proprietà Folder Funzionalità dell'ambiente Windows legacy , oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Funzionalità legacy dell'ambiente Windows, proprietà Folder
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102699"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="35dd9-106">Proprietà WebViewFolderContents.Folder</span><span class="sxs-lookup"><span data-stu-id="35dd9-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="35dd9-107">Ottiene un [**oggetto Folder**](../shell/folder.md) che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="35dd9-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="35dd9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="35dd9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dd9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35dd9-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="35dd9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="35dd9-110">Property value</span></span>

<span data-ttu-id="35dd9-111">Oggetto che riceve [**l'oggetto**](../shell/folder.md) Folder.</span><span class="sxs-lookup"><span data-stu-id="35dd9-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="35dd9-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="35dd9-112">Examples</span></span>

<span data-ttu-id="35dd9-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="35dd9-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="35dd9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35dd9-114">Requirements</span></span>



| <span data-ttu-id="35dd9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dd9-115">Requirement</span></span> | <span data-ttu-id="35dd9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="35dd9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dd9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35dd9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35dd9-118">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="35dd9-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35dd9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35dd9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35dd9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35dd9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35dd9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35dd9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35dd9-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="35dd9-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="35dd9-123">Idl</span><span class="sxs-lookup"><span data-stu-id="35dd9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35dd9-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="35dd9-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="35dd9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35dd9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35dd9-126"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="35dd9-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

