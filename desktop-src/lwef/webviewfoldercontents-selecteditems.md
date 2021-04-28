---
title: Metodo WebViewFolderContents.SelectedItems (Shldisp.h)
description: 'Metodo WebViewFolderContents.SelectedItems: ottiene un oggetto FolderItems che rappresenta tutti gli elementi selezionati nella visualizzazione.'
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Metodo SelectedItems Funzionalità legacy dell'ambiente Windows
- Metodo SelectedItems Funzionalità legacy dell'ambiente Windows, oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Funzionalità legacy dell'ambiente Windows, metodo SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102649"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="28872-106">Metodo WebViewFolderContents.SelectedItems</span><span class="sxs-lookup"><span data-stu-id="28872-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="28872-107">Ottiene un [**oggetto FolderItems**](../shell/folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="28872-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="28872-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28872-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="28872-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="28872-109">Parameters</span></span>

<span data-ttu-id="28872-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="28872-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28872-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28872-111">Return value</span></span>

<span data-ttu-id="28872-112">Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="28872-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="28872-113">Riferimento all'oggetto [**FolderItems.**](../shell/folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="28872-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="28872-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="28872-114">Examples</span></span>

<span data-ttu-id="28872-115">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="28872-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="28872-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28872-116">Requirements</span></span>



| <span data-ttu-id="28872-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28872-117">Requirement</span></span> | <span data-ttu-id="28872-118">Valore</span><span class="sxs-lookup"><span data-stu-id="28872-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28872-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28872-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28872-120">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="28872-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="28872-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28872-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28872-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28872-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="28872-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28872-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28872-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="28872-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="28872-125">Idl</span><span class="sxs-lookup"><span data-stu-id="28872-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28872-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="28872-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="28872-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28872-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28872-128"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="28872-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

