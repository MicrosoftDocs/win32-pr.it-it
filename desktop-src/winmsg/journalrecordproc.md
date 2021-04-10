---
UID: ''
title: Funzione di callback JournalRecordProc
description: La funzione registra i messaggi rimossi dal sistema dalla coda dei messaggi di sistema.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "103956291"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="75c13-103">JournalRecordProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="75c13-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="75c13-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75c13-104">Description</span></span>

<span data-ttu-id="75c13-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="75c13-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="75c13-106">La funzione registra i messaggi rimossi dal sistema dalla coda dei messaggi di sistema.</span><span class="sxs-lookup"><span data-stu-id="75c13-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="75c13-107">Successivamente, un'applicazione può usare una procedura di hook [JournalPlaybackProc](journalplaybackproc.md) per riprodurre i messaggi.</span><span class="sxs-lookup"><span data-stu-id="75c13-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="75c13-108">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="75c13-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="75c13-109">**JournalRecordProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="75c13-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="75c13-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="75c13-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="75c13-111">Codice [in]</span><span class="sxs-lookup"><span data-stu-id="75c13-111">code [in]</span></span>

<span data-ttu-id="75c13-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="75c13-112">Type: **int**</span></span>

<span data-ttu-id="75c13-113">Specifica la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="75c13-113">Specifies how to process the message.</span></span>
<span data-ttu-id="75c13-114">Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="75c13-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="75c13-115">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="75c13-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="75c13-116">Valore</span><span class="sxs-lookup"><span data-stu-id="75c13-116">Value</span></span> | <span data-ttu-id="75c13-117">Significato</span><span class="sxs-lookup"><span data-stu-id="75c13-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="75c13-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="75c13-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="75c13-119">Il parametro *lParam* è un puntatore a una struttura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) contenente informazioni su un messaggio rimosso dalla coda di sistema.</span><span class="sxs-lookup"><span data-stu-id="75c13-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="75c13-120">La procedura di hook deve registrare il contenuto della struttura copiando gli elementi in un buffer o in un file.</span><span class="sxs-lookup"><span data-stu-id="75c13-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="75c13-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="75c13-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="75c13-122">Una finestra di dialogo modale del sistema è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="75c13-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="75c13-123">La procedura di hook deve riprendere la registrazione.</span><span class="sxs-lookup"><span data-stu-id="75c13-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="75c13-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="75c13-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="75c13-125">Viene visualizzata una finestra di dialogo modale del sistema.</span><span class="sxs-lookup"><span data-stu-id="75c13-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="75c13-126">Finché la finestra di dialogo non viene distrutta, la procedura di hook deve arrestare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="75c13-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="75c13-127">wParam</span><span class="sxs-lookup"><span data-stu-id="75c13-127">wParam</span></span>

<span data-ttu-id="75c13-128">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="75c13-128">Type: **WPARAM**</span></span>

<span data-ttu-id="75c13-129">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="75c13-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="75c13-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="75c13-130">lParam [in]</span></span>

<span data-ttu-id="75c13-131">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="75c13-131">Type: **LPARAM**</span></span>

<span data-ttu-id="75c13-132">Puntatore a una struttura **EVENTMSG** contenente il messaggio da registrare.</span><span class="sxs-lookup"><span data-stu-id="75c13-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="75c13-133">Restituisce</span><span class="sxs-lookup"><span data-stu-id="75c13-133">Returns</span></span>

<span data-ttu-id="75c13-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="75c13-134">Type: **LRESULT**</span></span>

<span data-ttu-id="75c13-135">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="75c13-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c13-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="75c13-136">Remarks</span></span>

<span data-ttu-id="75c13-137">Una procedura di hook **JournalRecordProc** deve copiare ma non modificare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="75c13-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="75c13-138">Quando la routine hook restituisce il controllo al sistema, il messaggio continua a essere elaborato.</span><span class="sxs-lookup"><span data-stu-id="75c13-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="75c13-139">Installare la routine hook **JournalRecordProc** specificando il tipo di [WH_JOURNALRECORD](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="75c13-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="75c13-140">Non è necessario che una routine hook **JournalRecordProc** risieda in una libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="75c13-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="75c13-141">Una procedura di hook **JournalRecordProc** può risiedere nell'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="75c13-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="75c13-142">A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e [JournalPlaybackProc](journalplaybackproc.md) vengono sempre chiamate nel contesto del thread che imposta l'hook.</span><span class="sxs-lookup"><span data-stu-id="75c13-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="75c13-143">Un'applicazione che ha installato una procedura **JournalRecordProc** hook deve controllare il codice di chiave virtuale [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (implementato come combinazione di tasti Ctrl + Break sulla maggior parte delle tastiere).</span><span class="sxs-lookup"><span data-stu-id="75c13-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="75c13-144">Questo codice di chiave virtuale deve essere interpretato dall'applicazione come un segnale che l'utente desidera arrestare la registrazione del journal.</span><span class="sxs-lookup"><span data-stu-id="75c13-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="75c13-145">L'applicazione deve rispondere terminando la sequenza di registrazione e rimuovendo la procedura di hook **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="75c13-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="75c13-146">La rimozione è importante.</span><span class="sxs-lookup"><span data-stu-id="75c13-146">Removal is important.</span></span>
<span data-ttu-id="75c13-147">Impedisce a un'applicazione di inserimento nel journal di bloccare il sistema con una procedura di hook.</span><span class="sxs-lookup"><span data-stu-id="75c13-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="75c13-148">Questo ruolo come segnale per arrestare la registrazione di Journl significa che non è possibile registrare una combinazione di tasti CTRL + BREAK.</span><span class="sxs-lookup"><span data-stu-id="75c13-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="75c13-149">Poiché la combinazione di tasti CTRL + C non ha alcun ruolo come un segnale di inserimento nel journal, può essere registrata.</span><span class="sxs-lookup"><span data-stu-id="75c13-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="75c13-150">Sono disponibili altre due combinazioni di tasti che non possono essere registrate: CTRL + ESC e CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="75c13-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="75c13-151">Queste due combinazioni di tasti comportano l'arresto di tutte le attività di inserimento nel Journal (record o riproduzione), la rimozione di tutti gli hook di inserimento nel journal e la pubblicazione di un messaggio di [WM_CANCELJOURNAL](wm-canceljournal.md) nell'applicazione di inserimento nel journal.</span><span class="sxs-lookup"><span data-stu-id="75c13-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="75c13-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75c13-152">See also</span></span>

[<span data-ttu-id="75c13-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="75c13-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="75c13-154">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="75c13-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="75c13-155">JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="75c13-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="75c13-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="75c13-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="75c13-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="75c13-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="75c13-158">Hook</span><span class="sxs-lookup"><span data-stu-id="75c13-158">Hooks</span></span>](hooks.md)
