---
title: Metodo WebViewFolderContents.PopupItemMenu (Shldisp.h)
description: "Metodo WebViewFolderContents.PopupItemMenu: crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata."
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Metodo PopupItemMenu Funzionalità legacy dell'ambiente Windows
- Metodo PopupItemMenu Funzionalità legacy dell'ambiente Windows, oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Funzionalità legacy dell'ambiente Windows, metodo PopupItemMenu
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
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102639"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="ac6c3-106">Metodo WebViewFolderContents.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="ac6c3-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="ac6c3-107">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac6c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac6c3-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="ac6c3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac6c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac6c3-110">*vItem* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ac6c3-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac6c3-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ac6c3-111">Type: **Variant**</span></span>

<span data-ttu-id="ac6c3-112">Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà creato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="ac6c3-113">*vx* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ac6c3-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac6c3-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ac6c3-114">Type: **Variant**</span></span>

<span data-ttu-id="ac6c3-115">Posizione orizzontale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ac6c3-116">*vy* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ac6c3-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac6c3-117">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="ac6c3-117">Type: **Variant**</span></span>

<span data-ttu-id="ac6c3-118">Posizione verticale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac6c3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac6c3-119">Return value</span></span>

<span data-ttu-id="ac6c3-120">Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="ac6c3-120">Type: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="ac6c3-121">Quando questo metodo viene restituito, contiene la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="ac6c3-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="ac6c3-122">Examples</span></span>

<span data-ttu-id="ac6c3-123">L'esempio seguente illustra l'uso corretto **di PopupItemMenu** per JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="ac6c3-123">The following example shows the proper use of **PopupItemMenu** for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ac6c3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac6c3-124">Requirements</span></span>



| <span data-ttu-id="ac6c3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac6c3-125">Requirement</span></span> | <span data-ttu-id="ac6c3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ac6c3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6c3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac6c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac6c3-128">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ac6c3-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac6c3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac6c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac6c3-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac6c3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac6c3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac6c3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac6c3-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ac6c3-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ac6c3-133">Idl</span><span class="sxs-lookup"><span data-stu-id="ac6c3-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac6c3-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac6c3-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ac6c3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ac6c3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac6c3-136"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ac6c3-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

