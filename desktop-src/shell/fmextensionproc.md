---
description: Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.
title: Funzione di callback FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993688"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="8eb37-103">Funzione di callback FMExtensionProc</span><span class="sxs-lookup"><span data-stu-id="8eb37-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="8eb37-104">Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.</span><span class="sxs-lookup"><span data-stu-id="8eb37-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eb37-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="8eb37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eb37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb37-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8eb37-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb37-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="8eb37-108">Type: **HWND**</span></span>

<span data-ttu-id="8eb37-109">Handle di finestra per file Manager.</span><span class="sxs-lookup"><span data-stu-id="8eb37-109">A window handle to File Manager.</span></span> <span data-ttu-id="8eb37-110">Un'estensione utilizza questo handle per specificare la finestra padre per qualsiasi finestra di dialogo o finestra di messaggio che deve visualizzare e per inviare messaggi di query a gestione file.</span><span class="sxs-lookup"><span data-stu-id="8eb37-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="8eb37-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="8eb37-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb37-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="8eb37-112">Type: **WORD**</span></span>

<span data-ttu-id="8eb37-113">Uno dei seguenti messaggi di gestione file.</span><span class="sxs-lookup"><span data-stu-id="8eb37-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="8eb37-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**da 1 a 99**</span><span class="sxs-lookup"><span data-stu-id="8eb37-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-115">L'utente ha selezionato un elemento dal menu fornito dall'estensione.</span><span class="sxs-lookup"><span data-stu-id="8eb37-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="8eb37-116">Il valore è l'identificatore della voce di menu selezionata.</span><span class="sxs-lookup"><span data-stu-id="8eb37-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="8eb37-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**\_HELPMENUITEM FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-118">Premere F1 durante la selezione di un menu di estensione o di un elemento del comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="8eb37-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="8eb37-119">Indica che l'estensione deve chiamare **WinHelp** in modo appropriato per l'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="8eb37-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="8eb37-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**\_HELPSTRING FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-121">L'utente ha selezionato un menu di estensione o un elemento comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="8eb37-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="8eb37-122">Indica che l'estensione deve fornire una stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="8eb37-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="8eb37-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**\_INITMENU FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-124">L'utente ha selezionato il menu dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="8eb37-124">User selected the extension's menu.</span></span> <span data-ttu-id="8eb37-125">L'estensione deve inizializzare gli elementi nel menu.</span><span class="sxs-lookup"><span data-stu-id="8eb37-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="8eb37-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**\_carico FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-127">Gestione file sta caricando la DLL di estensione e richiede la DLL per informazioni sul menu fornito dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="8eb37-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="8eb37-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**\_selChange FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-129">La selezione nella finestra Directory di **file Manager** o nella finestra **Risultati ricerca** è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="8eb37-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="8eb37-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**\_TOOLBARLOAD FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-131">La barra degli strumenti viene creata da Gestione file e viene richiesta la DLL di estensione per informazioni sui pulsanti aggiunti dalla DLL alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="8eb37-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="8eb37-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_scaricamento FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-133">Il file Manager sta scaricando la DLL di estensione.</span><span class="sxs-lookup"><span data-stu-id="8eb37-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="8eb37-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_aggiornamento utente \_ FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="8eb37-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="8eb37-135">L'utente ha selezionato il comando **Aggiorna** dal menu **finestra** .</span><span class="sxs-lookup"><span data-stu-id="8eb37-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="8eb37-136">Se necessario, l'estensione deve aggiornare gli elementi nel menu.</span><span class="sxs-lookup"><span data-stu-id="8eb37-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8eb37-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8eb37-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb37-138">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8eb37-138">Type: **LONG**</span></span>

<span data-ttu-id="8eb37-139">Valore specifico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8eb37-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb37-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8eb37-140">Return value</span></span>

<span data-ttu-id="8eb37-141">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8eb37-141">Type: **LONG**</span></span>

<span data-ttu-id="8eb37-142">Restituisce un valore che dipende dal messaggio di parametro *wmsg* .</span><span class="sxs-lookup"><span data-stu-id="8eb37-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb37-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eb37-143">Requirements</span></span>



| <span data-ttu-id="8eb37-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb37-144">Requirement</span></span> | <span data-ttu-id="8eb37-145">Valore</span><span class="sxs-lookup"><span data-stu-id="8eb37-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb37-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb37-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb37-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8eb37-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8eb37-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb37-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb37-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8eb37-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8eb37-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eb37-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb37-151"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb37-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="8eb37-152">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8eb37-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8eb37-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8eb37-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




