---
UID: ''
title: Funzione di callback JournalPlaybackProc
description: Riproduce una serie di messaggi di mouse e tastiera registrati in precedenza.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "104398815"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="ae27a-103">JournalPlaybackProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="ae27a-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="ae27a-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae27a-104">Description</span></span>

<span data-ttu-id="ae27a-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="ae27a-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="ae27a-106">In genere, un'applicazione utilizza questa funzione per riprodurre una serie di messaggi di mouse e tastiera registrati in precedenza dalla procedura di hook **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="ae27a-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="ae27a-107">Finché viene installata una procedura **JournalPlaybackProc** Hook, l'input del mouse e della tastiera normale è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ae27a-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="ae27a-108">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="ae27a-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="ae27a-109">**JournalPlaybackProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="ae27a-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="ae27a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae27a-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="ae27a-111">Codice [in]</span><span class="sxs-lookup"><span data-stu-id="ae27a-111">code [in]</span></span>

<span data-ttu-id="ae27a-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ae27a-112">Type: **int**</span></span>

<span data-ttu-id="ae27a-113">Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ae27a-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="ae27a-114">Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="ae27a-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="ae27a-115">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ae27a-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="ae27a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ae27a-116">Value</span></span> | <span data-ttu-id="ae27a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ae27a-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="ae27a-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="ae27a-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="ae27a-119">La routine hook deve copiare il mouse o il messaggio della tastiera corrente nella struttura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) a cui punta il parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ae27a-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="ae27a-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="ae27a-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="ae27a-121">Un'applicazione ha chiamato la funzione [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg impostato su **PM_NOREMOVE**, a indicare che il messaggio non viene rimosso dalla coda di messaggi dopo l'elaborazione di **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="ae27a-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="ae27a-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="ae27a-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="ae27a-123">La procedura di hook deve prepararsi a copiare il mouse o il messaggio della tastiera successivo nella struttura **EVENTMSG** a cui punta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ae27a-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="ae27a-124">Quando riceve il codice di **HC_GETNEXT** , la routine hook deve copiare il messaggio nella struttura.</span><span class="sxs-lookup"><span data-stu-id="ae27a-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="ae27a-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="ae27a-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="ae27a-126">Una finestra di dialogo modale del sistema è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="ae27a-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="ae27a-127">La procedura di hook deve riprendere la riproduzione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="ae27a-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="ae27a-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="ae27a-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="ae27a-129">Viene visualizzata una finestra di dialogo modale del sistema.</span><span class="sxs-lookup"><span data-stu-id="ae27a-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="ae27a-130">Finché la finestra di dialogo non viene distrutta, la procedura di hook deve interrompere la riproduzione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="ae27a-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="ae27a-131">wParam</span><span class="sxs-lookup"><span data-stu-id="ae27a-131">wParam</span></span>

<span data-ttu-id="ae27a-132">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="ae27a-132">Type: **WPARAM**</span></span>

<span data-ttu-id="ae27a-133">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="ae27a-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="ae27a-134">lParam</span><span class="sxs-lookup"><span data-stu-id="ae27a-134">lParam</span></span>

<span data-ttu-id="ae27a-135">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="ae27a-135">Type: **LPARAM**</span></span>

<span data-ttu-id="ae27a-136">Puntatore a una struttura **EVENTMSG** che rappresenta un messaggio elaborato dalla routine hook.</span><span class="sxs-lookup"><span data-stu-id="ae27a-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="ae27a-137">Questo parametro è valido solo quando il parametro di *codice* è **HC_GETNEXT**.</span><span class="sxs-lookup"><span data-stu-id="ae27a-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="ae27a-138">Restituisce</span><span class="sxs-lookup"><span data-stu-id="ae27a-138">Returns</span></span>

<span data-ttu-id="ae27a-139">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ae27a-139">Type: **LRESULT**</span></span>

<span data-ttu-id="ae27a-140">Per fare in modo che il sistema attenda prima di elaborare il messaggio, il valore restituito deve corrispondere alla quantità di tempo, espressa in cicli di clock, che il sistema deve attendere.</span><span class="sxs-lookup"><span data-stu-id="ae27a-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="ae27a-141">(Questo valore può essere calcolato calcolando la differenza tra i membri temporali nei messaggi di input correnti e precedenti).</span><span class="sxs-lookup"><span data-stu-id="ae27a-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="ae27a-142">Per elaborare immediatamente il messaggio, il valore restituito deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ae27a-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="ae27a-143">Il valore restituito viene usato solo se il codice hook è **HC_GETNEXT**; in caso contrario, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ae27a-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae27a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae27a-144">Remarks</span></span>

<span data-ttu-id="ae27a-145">Una routine hook **JournalPlaybackProc** deve copiare un messaggio di input nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ae27a-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="ae27a-146">Il messaggio deve essere stato registrato in precedenza tramite una procedura di hook **JournalRecordProc** , che non deve modificare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="ae27a-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="ae27a-147">Per recuperare lo stesso messaggio ripetutamente, è possibile chiamare la procedura hook più volte con il parametro *Code* impostato su **HC_GETNEXT** senza una chiamata corrispondente con *codice* impostato su **HC_SKIP**.</span><span class="sxs-lookup"><span data-stu-id="ae27a-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="ae27a-148">Se il *codice* è **HC_GETNEXT** e il valore restituito è maggiore di zero, il sistema dorme per il numero di millisecondi specificato dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ae27a-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="ae27a-149">Quando il sistema continua, chiama di nuovo la routine hook con il *codice* impostato su **HC_GETNEXT** per recuperare lo stesso messaggio.</span><span class="sxs-lookup"><span data-stu-id="ae27a-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="ae27a-150">Il valore restituito da questa nuova chiamata a **JournalPlaybackProc** deve essere zero. in caso contrario, il sistema torna a dormire per il numero di millisecondi specificato dal valore restituito, chiama di nuovo **JournalPlaybackProc** e così via.</span><span class="sxs-lookup"><span data-stu-id="ae27a-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="ae27a-151">Il sistema sembra non rispondere.</span><span class="sxs-lookup"><span data-stu-id="ae27a-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="ae27a-152">A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e **JournalPlaybackProc** vengono sempre chiamate nel contesto del thread che imposta l'hook.</span><span class="sxs-lookup"><span data-stu-id="ae27a-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="ae27a-153">Quando la routine hook restituisce il controllo al sistema, il messaggio continua a essere elaborato.</span><span class="sxs-lookup"><span data-stu-id="ae27a-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="ae27a-154">Se il *codice* è **HC_SKIP**, la procedura di hook deve prepararsi a restituire il messaggio di evento registrato successivo alla chiamata successiva.</span><span class="sxs-lookup"><span data-stu-id="ae27a-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="ae27a-155">Installare la routine hook **JournalPlaybackProc** specificando il tipo di [WH_JOURNALPLAYBACK](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="ae27a-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="ae27a-156">Se l'utente preme CTRL + ESC o CTRL + ALT + CANC durante la riproduzione del Journal, il sistema interrompe la riproduzione, Annulla l'hook della procedura di riproduzione Journal e invia un messaggio di [WM_CANCELJOURNAL](wm-canceljournal.md) all'applicazione di inserimento nel journal.</span><span class="sxs-lookup"><span data-stu-id="ae27a-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="ae27a-157">Se la routine hook restituisce un messaggio nell'intervallo **WM_KEYFIRST** **WM_KEYLAST**, si applicano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae27a-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="ae27a-158">Il membro **paraml** della struttura **EVENTMSG** specifica il codice di chiave virtuale della chiave che è stata premuta.</span><span class="sxs-lookup"><span data-stu-id="ae27a-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="ae27a-159">Il membro **paramH** della struttura **EVENTMSG** specifica il codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="ae27a-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="ae27a-160">Non è possibile specificare un numero di ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="ae27a-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="ae27a-161">L'evento viene sempre impiegato per rappresentare un evento chiave.</span><span class="sxs-lookup"><span data-stu-id="ae27a-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae27a-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae27a-162">See also</span></span>

[<span data-ttu-id="ae27a-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="ae27a-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="ae27a-164">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="ae27a-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="ae27a-165">JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="ae27a-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="ae27a-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="ae27a-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="ae27a-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="ae27a-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="ae27a-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="ae27a-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="ae27a-169">Hook</span><span class="sxs-lookup"><span data-stu-id="ae27a-169">Hooks</span></span>](hooks.md)
