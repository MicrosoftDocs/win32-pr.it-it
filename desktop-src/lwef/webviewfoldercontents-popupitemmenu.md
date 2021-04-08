---
title: Metodo WebViewFolderContents. PopupItemMenu (shldisp. h)
description: Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Funzionalità dell'ambiente Windows legacy del metodo PopupItemMenu
- Funzionalità dell'ambiente Windows legacy del metodo PopupItemMenu, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, metodo PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740127"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="5834b-106">WebViewFolderContents. PopupItemMenu, metodo</span><span class="sxs-lookup"><span data-stu-id="5834b-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="5834b-107">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="5834b-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5834b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5834b-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="5834b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5834b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5834b-110">*vite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5834b-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5834b-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5834b-111">Type: **Variant**</span></span>

<span data-ttu-id="5834b-112">Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà creato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5834b-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="5834b-113">*VX* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5834b-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5834b-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5834b-114">Type: **Variant**</span></span>

<span data-ttu-id="5834b-115">Posizione orizzontale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5834b-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5834b-116">stato del  \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5834b-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5834b-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5834b-117">Type: **Variant**</span></span>

<span data-ttu-id="5834b-118">Posizione verticale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5834b-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5834b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5834b-119">Return value</span></span>

<span data-ttu-id="5834b-120">Tipo: \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="5834b-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="5834b-121">Quando termina, questo metodo contiene la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="5834b-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="5834b-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5834b-122">Examples</span></span>

<span data-ttu-id="5834b-123">Nell'esempio seguente viene illustrato l'uso corretto di _ *PopupItemMenu*\* per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="5834b-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



## <a name="requirements"></a><span data-ttu-id="5834b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5834b-124">Requirements</span></span>



| <span data-ttu-id="5834b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5834b-125">Requirement</span></span> | <span data-ttu-id="5834b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5834b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5834b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5834b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5834b-128">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5834b-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5834b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5834b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5834b-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5834b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5834b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5834b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5834b-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5834b-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5834b-133">IDL</span><span class="sxs-lookup"><span data-stu-id="5834b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5834b-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5834b-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5834b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5834b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5834b-136"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5834b-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

