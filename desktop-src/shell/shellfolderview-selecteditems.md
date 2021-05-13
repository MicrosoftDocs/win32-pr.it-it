---
description: 'Metodo ShellFolderView.SelectedItems: ottiene un oggetto FolderItems che rappresenta tutti gli elementi selezionati nella visualizzazione.'
title: Metodo ShellFolderView.SelectedItems (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: 485eda530adc4955abb27899d67ac0900eb0a910
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840742"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="89fa0-103">Metodo ShellFolderView.SelectedItems</span><span class="sxs-lookup"><span data-stu-id="89fa0-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="89fa0-104">Ottiene un [**oggetto FolderItems**](folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="89fa0-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fa0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89fa0-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="89fa0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89fa0-106">Parameters</span></span>

<span data-ttu-id="89fa0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="89fa0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89fa0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89fa0-108">Return value</span></span>

<span data-ttu-id="89fa0-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="89fa0-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="89fa0-110">Riferimento all'oggetto [**FolderItems.**](folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="89fa0-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89fa0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="89fa0-111">Remarks</span></span>

<span data-ttu-id="89fa0-112">**SelectedItems** può essere chiamato solo nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="89fa0-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="89fa0-113">Non funzionerà quando viene eseguito in una pagina Web tramite HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="89fa0-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="89fa0-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="89fa0-114">Examples</span></span>

<span data-ttu-id="89fa0-115">L'esempio seguente illustra l'uso corretto di questo metodo in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="89fa0-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
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
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="89fa0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89fa0-116">Requirements</span></span>



| <span data-ttu-id="89fa0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="89fa0-117">Requirement</span></span> | <span data-ttu-id="89fa0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="89fa0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fa0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89fa0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89fa0-120">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="89fa0-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="89fa0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89fa0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89fa0-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89fa0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89fa0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89fa0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89fa0-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="89fa0-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="89fa0-125">Idl</span><span class="sxs-lookup"><span data-stu-id="89fa0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89fa0-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="89fa0-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="89fa0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="89fa0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89fa0-128"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="89fa0-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




