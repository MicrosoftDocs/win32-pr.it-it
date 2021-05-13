---
description: Specifica una funzione di callback definita dall'applicazione chiamata da File Manager per comunicare con un'estensione di File Manager.
title: Funzione di callback FMExtensionProc (Wfext.h)
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
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842242"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="928d2-103">Funzione di callback FMExtensionProc</span><span class="sxs-lookup"><span data-stu-id="928d2-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="928d2-104">Specifica una funzione di callback definita dall'applicazione chiamata da File Manager per comunicare con un'estensione di File Manager.</span><span class="sxs-lookup"><span data-stu-id="928d2-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="928d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="928d2-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="928d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="928d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928d2-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="928d2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="928d2-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="928d2-108">Type: **HWND**</span></span>

<span data-ttu-id="928d2-109">Handle di finestra per File Manager.</span><span class="sxs-lookup"><span data-stu-id="928d2-109">A window handle to File Manager.</span></span> <span data-ttu-id="928d2-110">Un'estensione usa questo handle per specificare la finestra padre per qualsiasi finestra di dialogo o finestra di messaggio che deve visualizzare e per inviare messaggi di query a File Manager.</span><span class="sxs-lookup"><span data-stu-id="928d2-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="928d2-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="928d2-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="928d2-112">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="928d2-112">Type: **WORD**</span></span>

<span data-ttu-id="928d2-113">Uno dei messaggi di File Manager seguenti.</span><span class="sxs-lookup"><span data-stu-id="928d2-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="928d2-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**Da 1 a 99**</span><span class="sxs-lookup"><span data-stu-id="928d2-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-115">L'utente ha selezionato una voce dal menu fornito dall'estensione.</span><span class="sxs-lookup"><span data-stu-id="928d2-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="928d2-116">Il valore è l'identificatore della voce di menu selezionata.</span><span class="sxs-lookup"><span data-stu-id="928d2-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="928d2-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="928d2-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-118">L'utente ha premuto F1 durante la selezione di un menu di estensione o di un elemento di comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="928d2-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="928d2-119">Indica che l'estensione deve chiamare **WinHelp** in modo appropriato per l'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="928d2-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="928d2-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="928d2-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-121">L'utente ha selezionato un menu di estensione o una voce di comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="928d2-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="928d2-122">Indica che l'estensione deve fornire una stringa della Guida.</span><span class="sxs-lookup"><span data-stu-id="928d2-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="928d2-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="928d2-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-124">L'utente ha selezionato il menu dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="928d2-124">User selected the extension's menu.</span></span> <span data-ttu-id="928d2-125">L'estensione deve inizializzare le voci nel menu.</span><span class="sxs-lookup"><span data-stu-id="928d2-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="928d2-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**</span><span class="sxs-lookup"><span data-stu-id="928d2-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-127">Gestione file carica la DLL di estensione e richiede informazioni sul menu fornito dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="928d2-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="928d2-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="928d2-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-129">La selezione nella **finestra directory di File Manager** o nella finestra **Risultati** ricerca è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="928d2-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="928d2-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="928d2-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-131">Gestione file crea la barra degli strumenti e richiede alla DLL di estensione informazioni su eventuali pulsanti aggiunti dalla DLL alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="928d2-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="928d2-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**</span><span class="sxs-lookup"><span data-stu-id="928d2-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-133">Gestione file sta scaricando la DLL dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="928d2-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="928d2-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT \_ USER \_ REFRESH**</span><span class="sxs-lookup"><span data-stu-id="928d2-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="928d2-135">L'utente **ha selezionato** il comando Aggiorna dal menu Finestra. </span><span class="sxs-lookup"><span data-stu-id="928d2-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="928d2-136">Se necessario, l'estensione deve aggiornare le voci del menu.</span><span class="sxs-lookup"><span data-stu-id="928d2-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="928d2-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="928d2-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="928d2-138">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="928d2-138">Type: **LONG**</span></span>

<span data-ttu-id="928d2-139">Valore specifico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="928d2-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928d2-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="928d2-140">Return value</span></span>

<span data-ttu-id="928d2-141">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="928d2-141">Type: **LONG**</span></span>

<span data-ttu-id="928d2-142">Restituisce un valore dipendente dal messaggio *del parametro wMsg.*</span><span class="sxs-lookup"><span data-stu-id="928d2-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="928d2-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="928d2-143">Requirements</span></span>



| <span data-ttu-id="928d2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="928d2-144">Requirement</span></span> | <span data-ttu-id="928d2-145">Valore</span><span class="sxs-lookup"><span data-stu-id="928d2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="928d2-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="928d2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="928d2-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="928d2-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="928d2-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="928d2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="928d2-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="928d2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="928d2-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="928d2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="928d2-151"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="928d2-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="928d2-152">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="928d2-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="928d2-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="928d2-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




