---
description: Visualizza una finestra della guida che corrisponde all'impostazione della lingua dell'interfaccia utente corrente.
title: MLHtmlHelp (funzione)
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
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993800"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="d99dd-103">MLHtmlHelp (funzione)</span><span class="sxs-lookup"><span data-stu-id="d99dd-103">MLHtmlHelp function</span></span>

<span data-ttu-id="d99dd-104">\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d99dd-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d99dd-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d99dd-106">Visualizza una finestra della guida che corrisponde all'impostazione della lingua dell'interfaccia utente corrente.</span><span class="sxs-lookup"><span data-stu-id="d99dd-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d99dd-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="d99dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d99dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99dd-109">*hwndCaller* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99dd-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d99dd-110">Type: **HWND**</span></span>

<span data-ttu-id="d99dd-111">Handle per la finestra padre che chiama questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d99dd-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="d99dd-112">*pszFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99dd-113">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="d99dd-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="d99dd-114">Puntatore a un buffer che contiene il percorso completo di un file della Guida compilato (con estensione chm) o un file di argomento all'interno di un file della Guida specificato.</span><span class="sxs-lookup"><span data-stu-id="d99dd-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="d99dd-115">*uCommand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99dd-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d99dd-116">Type: **UINT**</span></span>

<span data-ttu-id="d99dd-117">Comando da completare.</span><span class="sxs-lookup"><span data-stu-id="d99dd-117">The command to complete.</span></span> <span data-ttu-id="d99dd-118">Questa funzione supporta direttamente solo [l' \_ \_ argomento di visualizzazione HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) e il [ \_ \_ \_ popup del testo visualizzato HH](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="d99dd-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="d99dd-119">Nel caso di qualsiasi altro comando, la chiamata viene trasmessa senza il valore di *dwCrossCodePage* a [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="d99dd-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="d99dd-120">*dwData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99dd-121">Tipo: **DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="d99dd-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="d99dd-122">Tutti i dati che potrebbero essere necessari, in base al valore del parametro *uCommand* .</span><span class="sxs-lookup"><span data-stu-id="d99dd-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d99dd-123">*dwCrossCodePage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99dd-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d99dd-124">Type: **DWORD**</span></span>

<span data-ttu-id="d99dd-125">Valore **DWORD** che indica la tabella codici dell'impostazione della lingua dell'interfaccia utente corrente, ad esempio CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="d99dd-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99dd-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d99dd-126">Return value</span></span>

<span data-ttu-id="d99dd-127">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d99dd-127">Type: **HWND**</span></span>

<span data-ttu-id="d99dd-128">A seconda del *uCommand* specificato e del risultato, **MLHtmlHelp** restituisce uno o entrambi gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d99dd-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="d99dd-129">Handle (HWND) della finestra della guida.</span><span class="sxs-lookup"><span data-stu-id="d99dd-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="d99dd-130">**Valore null**.</span><span class="sxs-lookup"><span data-stu-id="d99dd-130">**NULL**.</span></span> <span data-ttu-id="d99dd-131">In alcuni casi, **null** indica un errore. in altri casi, **null** indica che la finestra della guida non è stata ancora creata.</span><span class="sxs-lookup"><span data-stu-id="d99dd-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="d99dd-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="d99dd-132">Remarks</span></span>

<span data-ttu-id="d99dd-133">Se si verifica un problema con il percorso del file della Guida per la lingua corrente, la chiamata viene trasmessa a [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) per la gestione standard.</span><span class="sxs-lookup"><span data-stu-id="d99dd-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="d99dd-134">Quando la finestra della guida è chiusa, lo stato attivo torna al proprietario, a meno che il proprietario non sia il desktop.</span><span class="sxs-lookup"><span data-stu-id="d99dd-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="d99dd-135">Se *hwndCaller* è il desktop, il sistema operativo determina la posizione in cui viene restituito lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="d99dd-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="d99dd-136">Inoltre, se **MLHtmlHelp** invia messaggi di notifica dalla finestra della guida, i messaggi vengono inviati a *hwndCaller* , purché sia stata abilitata la verifica dei [messaggi di notifica](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) nella definizione della finestra della guida.</span><span class="sxs-lookup"><span data-stu-id="d99dd-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="d99dd-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="d99dd-137">Examples</span></span>

<span data-ttu-id="d99dd-138">Nell'esempio seguente viene chiamato il comando [HH \_ display \_ Topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) per aprire il file della Guida denominato Help. chm e visualizzare il relativo argomento predefinito nella finestra della guida denominata `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="d99dd-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="d99dd-139">In genere, la finestra della Guida specificata in questo comando è un [Visualizzatore della Guida HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)standard.</span><span class="sxs-lookup"><span data-stu-id="d99dd-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="d99dd-140">Quando si usa questa funzione, impostare la dimensione dello stack del file eseguibile di hosting su almeno 100.000.</span><span class="sxs-lookup"><span data-stu-id="d99dd-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="d99dd-141">Se la dimensione dello stack definita è troppo piccola, il thread creato per eseguire la Guida HTML verrà creato anche con questa dimensione dello stack e l'operazione potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="d99dd-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="d99dd-142">Facoltativamente, è possibile rimuovere/STACK dalla riga di comando del collegamento e rimuovere anche eventuali impostazioni dello STACK nel file DEF dell'eseguibile. in questo caso, la dimensione predefinita dello stack è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="d99dd-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="d99dd-143">È anche possibile impostare le dimensioni dello stack usando il comando del compilatore/fnumber (il compilatore lo passerà al linker come/STACK).</span><span class="sxs-lookup"><span data-stu-id="d99dd-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d99dd-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d99dd-144">Requirements</span></span>



| <span data-ttu-id="d99dd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d99dd-145">Requirement</span></span> | <span data-ttu-id="d99dd-146">Valore</span><span class="sxs-lookup"><span data-stu-id="d99dd-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d99dd-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d99dd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d99dd-148">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d99dd-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d99dd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d99dd-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d99dd-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d99dd-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d99dd-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d99dd-152"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="d99dd-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="d99dd-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d99dd-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d99dd-154"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d99dd-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d99dd-155">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d99dd-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d99dd-156">**MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d99dd-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
