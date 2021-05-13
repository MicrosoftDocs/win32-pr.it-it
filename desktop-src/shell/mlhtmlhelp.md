---
description: Visualizza una finestra della Guida che corrisponde all'impostazione corrente della lingua dell'interfaccia utente.
title: Funzione MLHtmlHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841212"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="70628-103">Funzione MLHtmlHelp</span><span class="sxs-lookup"><span data-stu-id="70628-103">MLHtmlHelp function</span></span>

<span data-ttu-id="70628-104">\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70628-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="70628-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70628-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="70628-106">Visualizza una finestra della Guida che corrisponde all'impostazione corrente della lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="70628-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="70628-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70628-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="70628-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70628-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70628-109">*hwndCaller* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="70628-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70628-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="70628-110">Type: **HWND**</span></span>

<span data-ttu-id="70628-111">Handle per la finestra padre che chiama questa funzione.</span><span class="sxs-lookup"><span data-stu-id="70628-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="70628-112">*pszFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="70628-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70628-113">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="70628-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="70628-114">Puntatore a un buffer che contiene il percorso completo di un file della Guida compilato (con estensione chm) o di un file di argomento all'interno di un file della Guida specificato.</span><span class="sxs-lookup"><span data-stu-id="70628-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="70628-115">*uCommand* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="70628-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70628-116">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="70628-116">Type: **UINT**</span></span>

<span data-ttu-id="70628-117">Comando da completare.</span><span class="sxs-lookup"><span data-stu-id="70628-117">The command to complete.</span></span> <span data-ttu-id="70628-118">Questa funzione supporta direttamente solo [HH \_ DISPLAY TOPIC \_ e](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) [HH DISPLAY TEXT \_ \_ \_ POPUP.](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command)</span><span class="sxs-lookup"><span data-stu-id="70628-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="70628-119">Nel caso di qualsiasi altro comando, la chiamata viene inoltrata senza il *valore dwCrossCodePage* a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="70628-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="70628-120">*dwData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="70628-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70628-121">Tipo: **DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="70628-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="70628-122">Tutti i dati che possono essere necessari, in base al valore del *parametro uCommand.*</span><span class="sxs-lookup"><span data-stu-id="70628-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70628-123">*dwCrossCodePage* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="70628-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70628-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70628-124">Type: **DWORD**</span></span>

<span data-ttu-id="70628-125">Valore **DWORD** che indica la tabella codici dell'impostazione corrente della lingua dell'interfaccia utente, ad esempio CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="70628-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70628-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70628-126">Return value</span></span>

<span data-ttu-id="70628-127">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="70628-127">Type: **HWND**</span></span>

<span data-ttu-id="70628-128">A seconda *dell'uCommand e* del risultato specificati, **MLHtmlHelp** restituisce uno o entrambi gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="70628-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="70628-129">Handle (hwnd) della finestra della Guida.</span><span class="sxs-lookup"><span data-stu-id="70628-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="70628-130">**NULL**.</span><span class="sxs-lookup"><span data-stu-id="70628-130">**NULL**.</span></span> <span data-ttu-id="70628-131">In alcuni casi, **NULL** indica un errore. in altri casi, **NULL** indica che la finestra della Guida non è ancora stata creata.</span><span class="sxs-lookup"><span data-stu-id="70628-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="70628-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="70628-132">Remarks</span></span>

<span data-ttu-id="70628-133">Se si verifica un problema con il percorso del file della Guida per la lingua corrente, la chiamata viene inoltrata a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) per la gestione standard.</span><span class="sxs-lookup"><span data-stu-id="70628-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="70628-134">Quando la finestra della Guida viene chiusa, lo stato attivo torna al proprietario, a meno che il proprietario non sia il desktop.</span><span class="sxs-lookup"><span data-stu-id="70628-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="70628-135">Se *hwndCaller* è il desktop, il sistema operativo determina dove viene restituito lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="70628-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="70628-136">Inoltre, se **MLHtmlHelp** invia messaggi di notifica dalla finestra della Guida, i messaggi vengono [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) inviati a *hwndCaller* purché sia stato abilitato il rilevamento dei messaggi di notifica nella definizione della finestra della Guida.</span><span class="sxs-lookup"><span data-stu-id="70628-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="70628-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="70628-137">Examples</span></span>

<span data-ttu-id="70628-138">Nell'esempio seguente viene chiamato il comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) per aprire il file della Guida denominato Help.chm e visualizzarne l'argomento predefinito nella finestra della Guida denominata `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="70628-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="70628-139">In genere, la finestra della Guida specificata in questo comando è un visualizzatore [della Guida HTML standard.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)</span><span class="sxs-lookup"><span data-stu-id="70628-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="70628-140">Quando si usa questa funzione, impostare le dimensioni dello stack del file eseguibile di hosting su almeno 100.000.</span><span class="sxs-lookup"><span data-stu-id="70628-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="70628-141">Se le dimensioni dello stack definite sono troppo piccole, verrà creato anche il thread creato per eseguire la Guida HTML con queste dimensioni dello stack e l'operazione potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="70628-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="70628-142">Facoltativamente, è possibile rimuovere /STACK dalla riga di comando del collegamento e anche rimuovere qualsiasi impostazione STACK nel file DEF del file eseguibile (in questo caso le dimensioni predefinite dello stack sono 1 MB).</span><span class="sxs-lookup"><span data-stu-id="70628-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="70628-143">È anche possibile impostare le dimensioni dello stack usando il comando del compilatore /Fnumber (il compilatore lo passerà al linker come /STACK).</span><span class="sxs-lookup"><span data-stu-id="70628-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70628-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70628-144">Requirements</span></span>



| <span data-ttu-id="70628-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="70628-145">Requirement</span></span> | <span data-ttu-id="70628-146">Valore</span><span class="sxs-lookup"><span data-stu-id="70628-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70628-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70628-147">Minimum supported client</span></span><br/> | <span data-ttu-id="70628-148">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="70628-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70628-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70628-149">Minimum supported server</span></span><br/> | <span data-ttu-id="70628-150">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70628-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70628-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70628-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="70628-152"><dt>Nessuna</dt></span><span class="sxs-lookup"><span data-stu-id="70628-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="70628-153">DLL</span><span class="sxs-lookup"><span data-stu-id="70628-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70628-154"><dt>Shlwapi.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="70628-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="70628-155">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="70628-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="70628-156">**MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="70628-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
