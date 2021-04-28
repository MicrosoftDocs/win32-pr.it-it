---
title: Metodo WebViewFolderContents.SelectItem (Shldisp.h)
description: 'Metodo WebViewFolderContents.SelectItem: imposta lo stato di selezione di un elemento nella visualizzazione.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Metodo SelectItem Funzionalità legacy dell'ambiente Windows
- Metodo SelectItem Funzionalità legacy dell'ambiente Windows, oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Funzionalità legacy dell'ambiente Windows, metodo SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102610"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="43cd6-106">Metodo WebViewFolderContents.SelectItem</span><span class="sxs-lookup"><span data-stu-id="43cd6-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="43cd6-107">Imposta lo stato di selezione di un elemento nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="43cd6-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="43cd6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43cd6-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="43cd6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43cd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cd6-110">*vItem* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="43cd6-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cd6-111">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="43cd6-111">Type: **Variant\***</span></span>

<span data-ttu-id="43cd6-112">Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà impostato lo stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="43cd6-112">The [**FolderItem**](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="43cd6-113">*dwFlags* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="43cd6-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cd6-114">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="43cd6-114">Type: **Integer**</span></span>

<span data-ttu-id="43cd6-115">Set di flag che indicano il nuovo stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="43cd6-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="43cd6-116">Può trattarsi di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="43cd6-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="43cd6-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="43cd6-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-118">Deselezionare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="43cd6-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="43cd6-119">(1)</span><span class="sxs-lookup"><span data-stu-id="43cd6-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-120">Selezionare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="43cd6-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="43cd6-121">(3)</span><span class="sxs-lookup"><span data-stu-id="43cd6-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-122">Mettere l'elemento in modalità di modifica.</span><span class="sxs-lookup"><span data-stu-id="43cd6-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="43cd6-123">(4)</span><span class="sxs-lookup"><span data-stu-id="43cd6-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-124">Deselezionare tutti gli elementi, ad esempio l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="43cd6-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="43cd6-125">(8)</span><span class="sxs-lookup"><span data-stu-id="43cd6-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-126">Verificare che l'elemento sia visualizzato nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="43cd6-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="43cd6-127">(16)</span><span class="sxs-lookup"><span data-stu-id="43cd6-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="43cd6-128">Assegnare all'elemento lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="43cd6-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cd6-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43cd6-129">Return value</span></span>

<span data-ttu-id="43cd6-130">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="43cd6-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="43cd6-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="43cd6-131">Examples</span></span>

<span data-ttu-id="43cd6-132">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="43cd6-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



## <a name="requirements"></a><span data-ttu-id="43cd6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43cd6-133">Requirements</span></span>



| <span data-ttu-id="43cd6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="43cd6-134">Requirement</span></span> | <span data-ttu-id="43cd6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="43cd6-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cd6-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43cd6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="43cd6-137">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="43cd6-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="43cd6-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43cd6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="43cd6-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43cd6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="43cd6-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43cd6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="43cd6-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="43cd6-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="43cd6-142">Idl</span><span class="sxs-lookup"><span data-stu-id="43cd6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43cd6-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="43cd6-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="43cd6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="43cd6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43cd6-145"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="43cd6-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

