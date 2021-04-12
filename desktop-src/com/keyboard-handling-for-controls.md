---
title: Gestione della tastiera per i controlli
description: Un controllo risponde agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332495"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="9c1e8-103">Gestione della tastiera per i controlli</span><span class="sxs-lookup"><span data-stu-id="9c1e8-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="9c1e8-104">Un controllo risponde agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="9c1e8-105">Il contenitore gestisce l'attività della tastiera per tutti i controlli incorporati.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="9c1e8-106">Con i documenti composti, i tasti di scelta rapida si applicano solo all'oggetto attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="9c1e8-107">Con i controlli, è stato aggiunto un meccanismo che consente a un controllo di rispondere ai tasti di scelta rapida anche se attualmente non è attiva l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="9c1e8-108">I metodi [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemonico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e il metodo [**IOleControlSite:: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) gestiscono i tasti di scelta rapida di un controllo.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="9c1e8-109">Una struttura [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descrive i tasti di scelta rapida di un controllo e i flag passati tramite il metodo **GetControlInfo** descrivono il comportamento dei controlli con i tasti Enter e ESC.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="9c1e8-110">Quando un controllo modifica i tasti di scelta, chiama **OnControlInfoChanged** , in modo che il contenitore possa ricaricare la struttura, se necessario.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="9c1e8-111">Quando un controllo è un'interfaccia utente attiva, è anche il controllo con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="9c1e8-112">Quando i controlli vengono attivati e disattivati tra l'oggetto attivo sul posto e gli Stati attivi dell'interfaccia utente, il controllo chiama [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) per indicare al contenitore le modifiche di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="9c1e8-113">Inoltre, quando un controllo è un'interfaccia utente attiva, avrà la prima possibilità di elaborare tutte le sequenze di tasti.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="9c1e8-114">Per fornire a un contenitore la possibilità di elaborare la sequenza di tasti prima del controllo, il controllo chiama [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="9c1e8-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="9c1e8-115">Se il contenitore non gestisce la sequenza di tasti, il controllo lo elabora.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c1e8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c1e8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c1e8-117">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="9c1e8-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




