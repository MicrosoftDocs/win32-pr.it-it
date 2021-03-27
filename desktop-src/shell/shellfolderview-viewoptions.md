---
description: Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Proprietà ShellFolderView. ViewOptions (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994992"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="3ed83-103">Proprietà ShellFolderView. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="3ed83-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="3ed83-104">Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ed83-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="3ed83-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3ed83-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed83-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ed83-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="3ed83-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3ed83-107">Property value</span></span>

<span data-ttu-id="3ed83-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto opzioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ed83-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="3ed83-109">Contiene uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ed83-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="3ed83-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="3ed83-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-111">L'opzione **Mostra tutti i file** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="3ed83-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="3ed83-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-113">L'opzione **Nascondi estensioni per i tipi di file noti** è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="3ed83-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="3ed83-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-115">L'opzione **Visualizza file compressi e cartelle con colore alternativo** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="3ed83-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="3ed83-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-117">L'opzione non **visualizzare i file nascosti** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="3ed83-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="3ed83-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-119">L'opzione **stile classico** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="3ed83-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="3ed83-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-121">Il **doppio clic per aprire un'opzione elemento** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3ed83-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="3ed83-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="3ed83-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="3ed83-123">L'opzione **Attiva desktop-Visualizza come pagina Web** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ed83-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ed83-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ed83-124">Remarks</span></span>

<span data-ttu-id="3ed83-125">[**FocusedItem**](shellfolderview-focuseditem.md) può essere chiamato solo sul sistema locale.</span><span class="sxs-lookup"><span data-stu-id="3ed83-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="3ed83-126">Non funzionerà se eseguita in una pagina Web su HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="3ed83-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="3ed83-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ed83-127">Examples</span></span>

<span data-ttu-id="3ed83-128">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo in JScript incorporato in HTML.</span><span class="sxs-lookup"><span data-stu-id="3ed83-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
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
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="3ed83-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ed83-129">Requirements</span></span>



| <span data-ttu-id="3ed83-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed83-130">Requirement</span></span> | <span data-ttu-id="3ed83-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3ed83-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed83-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ed83-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed83-133">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ed83-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ed83-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ed83-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed83-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ed83-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ed83-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ed83-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ed83-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed83-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3ed83-138">IDL</span><span class="sxs-lookup"><span data-stu-id="3ed83-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ed83-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ed83-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3ed83-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed83-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed83-141"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3ed83-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
