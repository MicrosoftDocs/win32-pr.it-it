---
UID: ''
title: Funzione di callback ShellProc
description: La funzione riceve le notifiche degli eventi della shell dal sistema.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299556"
---
# <a name="shellproc-function"></a><span data-ttu-id="a09bd-103">ShellProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="a09bd-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="a09bd-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a09bd-104">Description</span></span>

<span data-ttu-id="a09bd-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="a09bd-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="a09bd-106">La funzione riceve le notifiche degli eventi della shell dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a09bd-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="a09bd-107">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="a09bd-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="a09bd-108">**ShellProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="a09bd-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="a09bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a09bd-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="a09bd-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="a09bd-110">nCode [in]</span></span>

<span data-ttu-id="a09bd-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="a09bd-111">Type: **int**</span></span>

<span data-ttu-id="a09bd-112">Codice hook.</span><span class="sxs-lookup"><span data-stu-id="a09bd-112">The hook code.</span></span>
<span data-ttu-id="a09bd-113">Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="a09bd-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a09bd-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="a09bd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a09bd-115">Value</span></span> | <span data-ttu-id="a09bd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a09bd-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="a09bd-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="a09bd-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="a09bd-118">Lo stato di accessibilità è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="a09bd-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="a09bd-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="a09bd-120">La shell deve attivare la finestra principale.</span><span class="sxs-lookup"><span data-stu-id="a09bd-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="a09bd-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="a09bd-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="a09bd-122">L'utente ha completato un evento di input (ad esempio, ha premuto un pulsante di comando dell'applicazione sul mouse o un tasto di comando dell'applicazione sulla tastiera) e l'applicazione non ha gestito il messaggio [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) generato da tale input.</span><span class="sxs-lookup"><span data-stu-id="a09bd-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="a09bd-123">Se la routine della shell gestisce il messaggio di [WM_COMMAND](/windows/desktop/menurc/wm-command) , non deve chiamare **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="a09bd-124">Per ulteriori informazioni, vedere la sezione valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a09bd-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="a09bd-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="a09bd-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="a09bd-126">Una finestra viene ridotta A icona o ingrandita.</span><span class="sxs-lookup"><span data-stu-id="a09bd-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="a09bd-127">Il sistema richiede le coordinate del rettangolo ridotto a icona per la finestra.</span><span class="sxs-lookup"><span data-stu-id="a09bd-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="a09bd-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="a09bd-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="a09bd-129">La lingua della tastiera è stata modificata o è stato caricato un nuovo layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="a09bd-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="a09bd-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="a09bd-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="a09bd-131">Il titolo di una finestra nella barra delle applicazioni è stato ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="a09bd-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="a09bd-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="a09bd-133">L'utente ha selezionato l'elenco attività.</span><span class="sxs-lookup"><span data-stu-id="a09bd-133">The user has selected the task list.</span></span> <span data-ttu-id="a09bd-134">Un'applicazione shell che fornisce un elenco attività deve restituire **true** per impedire che Windows avvii l'elenco attività.</span><span class="sxs-lookup"><span data-stu-id="a09bd-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="a09bd-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="a09bd-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="a09bd-136">L'attivazione è stata modificata in un'altra finestra di primo livello, senza proprietario.</span><span class="sxs-lookup"><span data-stu-id="a09bd-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="a09bd-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="a09bd-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="a09bd-138">È stata creata una finestra di primo livello, senza proprietario.</span><span class="sxs-lookup"><span data-stu-id="a09bd-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="a09bd-139">La finestra esiste quando il sistema chiama questo hook.</span><span class="sxs-lookup"><span data-stu-id="a09bd-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="a09bd-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="a09bd-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="a09bd-141">Una finestra di primo livello non di proprietà sta per essere distrutta.</span><span class="sxs-lookup"><span data-stu-id="a09bd-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="a09bd-142">La finestra esiste ancora quando il sistema chiama questo hook.</span><span class="sxs-lookup"><span data-stu-id="a09bd-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="a09bd-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="a09bd-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="a09bd-144">È in corso la sostituzione di una finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="a09bd-144">A top-level window is being replaced.</span></span> <span data-ttu-id="a09bd-145">La finestra esiste quando il sistema chiama questo hook.</span><span class="sxs-lookup"><span data-stu-id="a09bd-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="a09bd-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="a09bd-146">wParam [in]</span></span>

<span data-ttu-id="a09bd-147">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="a09bd-147">Type: **WPARAM**</span></span>

<span data-ttu-id="a09bd-148">Questo parametro dipende dal valore del parametro *nCode* , come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a09bd-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="a09bd-149">nCode</span><span class="sxs-lookup"><span data-stu-id="a09bd-149">nCode</span></span> | <span data-ttu-id="a09bd-150">wParam</span><span class="sxs-lookup"><span data-stu-id="a09bd-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="a09bd-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="a09bd-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="a09bd-152">Indica quale funzionalità di accessibilità ha modificato lo stato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="a09bd-153">Questo valore è uno dei seguenti: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** o **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="a09bd-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="a09bd-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="a09bd-155">Indica la posizione in cui è stato originariamente inviato il messaggio di **WM_APPCOMMAND** ; ad esempio, l'handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="a09bd-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="a09bd-156">Per ulteriori informazioni, vedere parametro cmd in **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="a09bd-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="a09bd-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="a09bd-158">Handle per la finestra ridotta a icona o ingrandita.</span><span class="sxs-lookup"><span data-stu-id="a09bd-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="a09bd-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="a09bd-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="a09bd-160">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="a09bd-160">A handle to the window.</span></span> |
| <span data-ttu-id="a09bd-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="a09bd-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="a09bd-162">Handle per la finestra ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="a09bd-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="a09bd-164">Handle per la finestra attivata.</span><span class="sxs-lookup"><span data-stu-id="a09bd-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="a09bd-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="a09bd-166">Handle per la finestra creata.</span><span class="sxs-lookup"><span data-stu-id="a09bd-166">A handle to the created window.</span></span> |
| <span data-ttu-id="a09bd-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="a09bd-168">Handle per la finestra distrutta.</span><span class="sxs-lookup"><span data-stu-id="a09bd-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="a09bd-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="a09bd-170">Handle per la finestra da sostituire.</span><span class="sxs-lookup"><span data-stu-id="a09bd-170">A handle to the window being replaced.</span></span> <span data-ttu-id="a09bd-171">Windows 2000: non supportato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="a09bd-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="a09bd-172">lParam [in]</span></span>

<span data-ttu-id="a09bd-173">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="a09bd-173">Type: **LPARAM**</span></span>

<span data-ttu-id="a09bd-174">Questo parametro dipende dal valore del parametro *nCode* , come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a09bd-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="a09bd-175">nCode</span><span class="sxs-lookup"><span data-stu-id="a09bd-175">nCode</span></span> | <span data-ttu-id="a09bd-176">lParam</span><span class="sxs-lookup"><span data-stu-id="a09bd-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="a09bd-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="a09bd-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="a09bd-178">`GET_APPCOMMAND_LPARAM(lParam)` comando dell'applicazione corrispondente all'evento di input.</span><span class="sxs-lookup"><span data-stu-id="a09bd-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="a09bd-179">`GET_DEVICE_LPARAM(lParam)` indica la generazione dell'evento di input. ad esempio, il mouse o la tastiera.</span><span class="sxs-lookup"><span data-stu-id="a09bd-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="a09bd-180">Per ulteriori informazioni, vedere la descrizione del parametro *Udevice* in **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="a09bd-181">`GET_FLAGS_LPARAM(lParam)` dipende dal valore di *cmd* in **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="a09bd-182">Ad esempio, potrebbe indicare quali chiavi virtuali sono state mantenute al momento dell'invio del messaggio di **WM_APPCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="a09bd-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="a09bd-183">Per ulteriori informazioni, vedere il parametro *dwCmdFlags* description in **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="a09bd-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="a09bd-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="a09bd-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="a09bd-185">Puntatore a una struttura [Rect](/previous-versions/dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a09bd-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="a09bd-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="a09bd-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="a09bd-187">Handle per un layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="a09bd-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="a09bd-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="a09bd-189">Handle per la finestra che è stato spostato in un monitor diverso.</span><span class="sxs-lookup"><span data-stu-id="a09bd-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="a09bd-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="a09bd-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="a09bd-191">Il valore è **true** se la finestra è lampeggiante o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a09bd-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="a09bd-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="a09bd-193">Il valore è TRUE se la finestra è in modalità schermo intero oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a09bd-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="a09bd-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="a09bd-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="a09bd-195">Handle per la nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="a09bd-195">A handle to the new window.</span></span> <span data-ttu-id="a09bd-196">Windows 2000: non supportato.</span><span class="sxs-lookup"><span data-stu-id="a09bd-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="a09bd-197">Restituisce</span><span class="sxs-lookup"><span data-stu-id="a09bd-197">Returns</span></span>

<span data-ttu-id="a09bd-198">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a09bd-198">Type: **LRESULT**</span></span>

<span data-ttu-id="a09bd-199">Il valore restituito deve essere zero, a meno che il valore di nCode non sia **HSHELL_APPCOMMAND** e la routine della shell gestisca il messaggio di **WM_COMMAND** .</span><span class="sxs-lookup"><span data-stu-id="a09bd-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="a09bd-200">In questo caso, il valore restituito deve essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a09bd-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a09bd-201">Commenti</span><span class="sxs-lookup"><span data-stu-id="a09bd-201">Remarks</span></span>

<span data-ttu-id="a09bd-202">Installare questa routine hook specificando il tipo di hook [WH_SHELL](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="a09bd-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="a09bd-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a09bd-203">See also</span></span>

[<span data-ttu-id="a09bd-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="a09bd-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="a09bd-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="a09bd-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="a09bd-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="a09bd-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="a09bd-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a09bd-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="a09bd-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="a09bd-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="a09bd-209">Hook</span><span class="sxs-lookup"><span data-stu-id="a09bd-209">Hooks</span></span>](hooks.md)
