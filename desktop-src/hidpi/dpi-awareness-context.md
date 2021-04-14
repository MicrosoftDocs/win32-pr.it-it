---
title: Handle di DPI_AWARENESS_CONTEXT (windef. h)
description: Identifica il contesto di consapevolezza per una finestra.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340752"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="28f08-103">Handle del contesto di \_ consapevolezza dpi \_</span><span class="sxs-lookup"><span data-stu-id="28f08-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="28f08-104">Identifica il contesto di consapevolezza per una finestra.</span><span class="sxs-lookup"><span data-stu-id="28f08-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28f08-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="28f08-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="28f08-106">Constants</span></span>

<span data-ttu-id="28f08-107">**contesto di consapevolezza DPI non \_ \_ \_ consapevole**</span><span class="sxs-lookup"><span data-stu-id="28f08-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="28f08-108">Valori DPI non compatibili.</span><span class="sxs-lookup"><span data-stu-id="28f08-108">DPI unaware.</span></span> <span data-ttu-id="28f08-109">Questa finestra non viene ridimensionata per le modifiche DPI e si presuppone sempre un fattore di scala pari a 100% (96 DPI).</span><span class="sxs-lookup"><span data-stu-id="28f08-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="28f08-110">Il sistema verrà ridimensionato automaticamente in base a qualsiasi altra impostazione DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="28f08-111">**\_riconoscimento del \_ sistema del contesto \_ \_ di compatibilità dpi**</span><span class="sxs-lookup"><span data-stu-id="28f08-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="28f08-112">Compatibile con DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="28f08-112">System DPI aware.</span></span> <span data-ttu-id="28f08-113">Questa finestra non viene ridimensionata per le modifiche DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="28f08-114">Eseguirà una query per il valore DPI una volta e utilizzerà tale valore per la durata del processo.</span><span class="sxs-lookup"><span data-stu-id="28f08-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="28f08-115">Se il valore DPI viene modificato, il processo non si adatterà al nuovo valore DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="28f08-116">Il valore verrà automaticamente scalato verso l'alto o verso il basso dal sistema in caso di variazione del valore DPI rispetto al valore di sistema.</span><span class="sxs-lookup"><span data-stu-id="28f08-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="28f08-117">**\_contesto di consapevolezza dpi \_ \_ per \_ monitoraggio \_**</span><span class="sxs-lookup"><span data-stu-id="28f08-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="28f08-118">Per il monitor compatibile con DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-118">Per monitor DPI aware.</span></span> <span data-ttu-id="28f08-119">Questa finestra Controlla il valore DPI quando viene creato e regola il fattore di scala ogni volta che viene modificato il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="28f08-120">Questi processi non vengono ridimensionati automaticamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="28f08-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="28f08-121">**\_Contesto di riconoscimento dpi \_ \_ per monitoraggio con \_ \_ riconoscimento \_ v2**</span><span class="sxs-lookup"><span data-stu-id="28f08-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="28f08-122">Noto anche come **per il monitor V2**.</span><span class="sxs-lookup"><span data-stu-id="28f08-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="28f08-123">Avanzamento rispetto alla modalità di riconoscimento DPI per monitor originale, che consente alle applicazioni di accedere ai nuovi comportamenti di ridimensionamento correlati a DPI in base a una finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="28f08-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="28f08-124">Per monitor V2 è stato reso disponibile nell'aggiornamento dei creatori di Windows 10 e non è disponibile nelle versioni precedenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28f08-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="28f08-125">I comportamenti aggiuntivi introdotti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="28f08-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="28f08-126">**Notifiche di modifica del valore dpi della finestra figlio** : in per i contesti di monitoraggio V2, l'intero albero della finestra riceve una notifica delle modifiche DPI che si verificano.</span><span class="sxs-lookup"><span data-stu-id="28f08-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="28f08-127">**Ridimensionamento dell'area non client** : tutte le finestre avranno automaticamente un'area non client disegnata in modo sensibile ai DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="28f08-128">Le chiamate a [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="28f08-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="28f08-129">**Ridimensionamento dei menu Win32** : tutti i menu Ntuser creati nei contesti per monitor V2 verranno ridimensionati in base al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="28f08-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="28f08-130">**Ridimensionamento della finestra di dialogo** : le finestre di dialogo Win32 create nei contesti per monitor V2 risponderanno automaticamente alle modifiche DPI.</span><span class="sxs-lookup"><span data-stu-id="28f08-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="28f08-131">**Miglioramento della scalabilità dei controlli comctl32: i** vari controlli comctl32 hanno migliorato il comportamento di scalabilità dpi in per i contesti di monitoraggio V2.</span><span class="sxs-lookup"><span data-stu-id="28f08-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="28f08-132">**Miglioramento del comportamento del tema** : gli handle di uxtheme aperti nel contesto di una finestra per monitor V2 funzioneranno in termini di dpi associato a tale finestra.</span><span class="sxs-lookup"><span data-stu-id="28f08-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="28f08-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="28f08-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="28f08-134">DPI non è a conoscenza della migliore qualità del contenuto basato su GDI.</span><span class="sxs-lookup"><span data-stu-id="28f08-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="28f08-135">Questa modalità si comporta in modo analogo a DPI_AWARENESS_CONTEXT_UNAWARE, ma consente inoltre al sistema di migliorare automaticamente la qualità di rendering del testo e di altre primitive basate su GDI quando la finestra viene visualizzata in un monitor con valori DPI alti.</span><span class="sxs-lookup"><span data-stu-id="28f08-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="28f08-136">Per informazioni dettagliate, vedere [miglioramento dell'esperienza con valori DPI elevati nelle app desktop basate su GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="28f08-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="28f08-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED è stato introdotto nell'aggiornamento del 2018 ottobre di Windows 10 (noto anche come versione 1809).</span><span class="sxs-lookup"><span data-stu-id="28f08-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="28f08-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28f08-138">Requirements</span></span>

| <span data-ttu-id="28f08-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="28f08-139">Requirement</span></span> | <span data-ttu-id="28f08-140">Valore</span><span class="sxs-lookup"><span data-stu-id="28f08-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="28f08-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28f08-141">Minimum supported client</span></span><br/> | <span data-ttu-id="28f08-142">Solo app desktop Windows 10 versione 1607 \[\]</span><span class="sxs-lookup"><span data-stu-id="28f08-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="28f08-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28f08-143">Minimum supported server</span></span><br/> | <span data-ttu-id="28f08-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="28f08-144">None supported</span></span> <br/>  |
| <span data-ttu-id="28f08-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28f08-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f08-146"><dt>windef. h</dt></span><span class="sxs-lookup"><span data-stu-id="28f08-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="28f08-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28f08-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f08-148">**AreDpiAwarenessContextsEqual**</span><span class="sxs-lookup"><span data-stu-id="28f08-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="28f08-149">**GetAwarenessFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-150">**GetDpiFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-151">**GetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-152">**GetWindowDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-153">**IsValidDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-154">**SetProcessDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="28f08-155">**SetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="28f08-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
