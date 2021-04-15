---
title: Proprietà WebViewFolderContents.Folder (Shldisp.h)
description: Ottiene un oggetto cartella che rappresenta la visualizzazione.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Proprietà cartella caratteristiche ambiente Windows legacy
- Proprietà cartella caratteristiche dell'ambiente Windows legacy, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà Folder
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
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475424"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="dc506-106">Proprietà WebViewFolderContents. Folder</span><span class="sxs-lookup"><span data-stu-id="dc506-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="dc506-107">Ottiene un oggetto [**cartella**](../shell/folder.md) che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc506-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="dc506-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dc506-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc506-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc506-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="dc506-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dc506-110">Property value</span></span>

<span data-ttu-id="dc506-111">Oggetto che riceve l'oggetto [**cartella**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="dc506-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="dc506-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc506-112">Examples</span></span>

<span data-ttu-id="dc506-113">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="dc506-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="dc506-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc506-114">Requirements</span></span>



| <span data-ttu-id="dc506-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc506-115">Requirement</span></span> | <span data-ttu-id="dc506-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dc506-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc506-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc506-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc506-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc506-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dc506-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc506-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc506-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc506-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc506-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc506-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc506-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc506-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dc506-123">IDL</span><span class="sxs-lookup"><span data-stu-id="dc506-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc506-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc506-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dc506-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dc506-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc506-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="dc506-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

