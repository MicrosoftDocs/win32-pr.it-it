---
description: Imposta lo stato di selezione di un elemento nella visualizzazione.
title: Metodo ShellFolderView. SelectItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233194"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="d2d7d-103">ShellFolderView. SelectItem, metodo</span><span class="sxs-lookup"><span data-stu-id="d2d7d-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="d2d7d-104">Imposta lo stato di selezione di un elemento nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2d7d-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="d2d7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2d7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d7d-107">*vite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2d7d-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d7d-108">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="d2d7d-108">Type: \**Variant\** _</span></span>

<span data-ttu-id="d2d7d-109">Oggetto [_ *FolderItem* \*](folderitem.md) per il quale verrà impostato lo stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-109">The [_ *FolderItem*\*](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="d2d7d-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2d7d-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d7d-111">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-111">Type: **Integer**</span></span>

<span data-ttu-id="d2d7d-112">Set di flag che indicano il nuovo stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="d2d7d-113">Può corrispondere a uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="d2d7d-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-115">Deselezionare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="d2d7d-116">(1)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-117">Selezionare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="d2d7d-118">(3)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-119">Inserire l'elemento in modalità di modifica.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="d2d7d-120">(4)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-121">Deseleziona tutto tranne l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="d2d7d-122">(8)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-123">Verificare che l'elemento sia visualizzato nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="d2d7d-124">(16)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d2d7d-125">Assegnare all'elemento lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d7d-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2d7d-126">Return value</span></span>

<span data-ttu-id="d2d7d-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d7d-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2d7d-128">Remarks</span></span>

<span data-ttu-id="d2d7d-129">[**FocusedItem**](shellfolderview-focuseditem.md) può essere chiamato solo sul sistema locale.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="d2d7d-130">Non funzionerà se eseguita in una pagina Web su HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="d2d7d-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2d7d-131">Examples</span></span>

<span data-ttu-id="d2d7d-132">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="d2d7d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2d7d-133">Requirements</span></span>



| <span data-ttu-id="d2d7d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d7d-134">Requirement</span></span> | <span data-ttu-id="d2d7d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d2d7d-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d7d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d7d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d7d-137">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2d7d-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d2d7d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d7d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d7d-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2d7d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2d7d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2d7d-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d7d-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d2d7d-142">IDL</span><span class="sxs-lookup"><span data-stu-id="d2d7d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2d7d-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2d7d-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d2d7d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d7d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d7d-145"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d2d7d-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




