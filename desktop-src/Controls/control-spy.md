---
title: Controllare Spy v 2.0
description: Control Spy è uno strumento che aiuta gli sviluppatori a comprendere i controlli comuni su come applicare gli stili e come rispondono a messaggi e notifiche.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047528"
---
# <a name="control-spy-v20"></a><span data-ttu-id="c1a81-103">Controllare Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1a81-103">Control Spy v2.0</span></span>

<span data-ttu-id="c1a81-104">Controllo Spy è uno strumento che consente agli sviluppatori di comprendere i controlli comuni: come applicare gli stili e come rispondono a messaggi e notifiche.</span><span class="sxs-lookup"><span data-stu-id="c1a81-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="c1a81-105">Utilizzando Spy Control, è possibile visualizzare immediatamente il modo in cui gli stili diversi influiscono sul comportamento e sull'aspetto di ogni controllo e su come è possibile modificare lo stato di ogni controllo inviando messaggi.</span><span class="sxs-lookup"><span data-stu-id="c1a81-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="c1a81-106">Sono disponibili due versioni di Spy Control, una per [Comctl32.dll versione 5. x](common-control-versions.md) e una per Comctl32.dll versione 6,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="c1a81-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="c1a81-107">ControlSpyV6.exe dispone di un manifesto dell'applicazione incorporato in modo che utilizzi i controlli con tema più recenti.</span><span class="sxs-lookup"><span data-stu-id="c1a81-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="c1a81-108">ControlSpyV5.exe non dispone di questo manifesto e pertanto il valore predefinito è la versione precedente.</span><span class="sxs-lookup"><span data-stu-id="c1a81-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="c1a81-109">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1a81-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c1a81-110">Overview</span><span class="sxs-lookup"><span data-stu-id="c1a81-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="c1a81-111">Stili</span><span class="sxs-lookup"><span data-stu-id="c1a81-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="c1a81-112">Messaggi</span><span class="sxs-lookup"><span data-stu-id="c1a81-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="c1a81-113">Dimensioni/colore</span><span class="sxs-lookup"><span data-stu-id="c1a81-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="c1a81-114">Dove ottenere il controllo Spy</span><span class="sxs-lookup"><span data-stu-id="c1a81-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="c1a81-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1a81-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="c1a81-116">Panoramica</span><span class="sxs-lookup"><span data-stu-id="c1a81-116">Overview</span></span>

<span data-ttu-id="c1a81-117">Il controllo Spy ospita un controllo comune selezionato al centro della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1a81-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="c1a81-118">È possibile modificare il controllo visualizzato selezionando diversi controlli dalla casella di riepilogo sul lato sinistro della finestra.</span><span class="sxs-lookup"><span data-stu-id="c1a81-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="c1a81-119">I messaggi o le notifiche ricevute dal controllo verranno elencati sul lato destro della finestra man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="c1a81-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="c1a81-120">È possibile abilitare o disabilitare questa funzionalità usando le caselle di controllo **messaggi ricevuti** e **notifiche ricevute** .</span><span class="sxs-lookup"><span data-stu-id="c1a81-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="c1a81-121">La figura seguente mostra l'applicazione Control Spy.</span><span class="sxs-lookup"><span data-stu-id="c1a81-121">The following image shows the Control Spy application.</span></span>

![finestra Spy di controllo](images/controlspy-main.png)

<span data-ttu-id="c1a81-123">Nella parte inferiore della finestra sono disponibili diverse schede in cui sono presenti più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c1a81-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="c1a81-124">Stili</span><span class="sxs-lookup"><span data-stu-id="c1a81-124">Styles</span></span>

<span data-ttu-id="c1a81-125">La scheda **stili** consente di modificare lo stile della finestra corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="c1a81-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="c1a81-126">Selezionare o deselezionare uno degli stili elencati, quindi fare clic sul pulsante **applica** per modificare lo stile del controllo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c1a81-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="c1a81-127">In alternativa, è possibile usare il pulsante **ricrea** per creare un nuovo controllo con gli stili selezionati.</span><span class="sxs-lookup"><span data-stu-id="c1a81-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="c1a81-128">Il pulsante **Reimposta** restituirà il controllo agli stili predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c1a81-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="c1a81-129">I pulsanti copia **stile** e **copia ExStyle** sotto la scheda copieranno le costanti di stile selezionate negli Appunti come elenco delimitato or bit per bit ( \| ).</span><span class="sxs-lookup"><span data-stu-id="c1a81-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="c1a81-130">È possibile incollare questo elenco direttamente nella chiamata a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per fornire un controllo nella propria applicazione con lo stesso stile.</span><span class="sxs-lookup"><span data-stu-id="c1a81-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="c1a81-131">La figura seguente mostra la scheda **stili** per un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="c1a81-131">The following image shows the **Styles** tab for a button control.</span></span>

![scheda stili spia di controllo](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="c1a81-133">Messaggi</span><span class="sxs-lookup"><span data-stu-id="c1a81-133">Messages</span></span>

<span data-ttu-id="c1a81-134">La scheda **messaggi** consente di inviare quasi tutti i messaggi a un controllo.</span><span class="sxs-lookup"><span data-stu-id="c1a81-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="c1a81-135">Dopo aver selezionato un messaggio dalla casella di riepilogo, è possibile immettere i dati inviati come parametri *wParam* e *lParam* della chiamata a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="c1a81-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="c1a81-136">Dopo aver fatto clic su **Invia**, il messaggio viene inviato al controllo e tutti i risultati vengono visualizzati nella casella di testo nella parte inferiore della scheda.</span><span class="sxs-lookup"><span data-stu-id="c1a81-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="c1a81-137">La figura seguente mostra la scheda messaggi quando viene selezionato un messaggio specifico.</span><span class="sxs-lookup"><span data-stu-id="c1a81-137">The following image shows the messages tab when a particular message is selected.</span></span>

![scheda messaggi di controllo Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="c1a81-139">Dimensioni/colore</span><span class="sxs-lookup"><span data-stu-id="c1a81-139">Size/Color</span></span>

<span data-ttu-id="c1a81-140">La scheda **dimensioni/colore** può essere utilizzata per modificare le dimensioni del controllo e il colore dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="c1a81-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="c1a81-141">Dove ottenere il controllo Spy</span><span class="sxs-lookup"><span data-stu-id="c1a81-141">Where to Get Control Spy</span></span>

<span data-ttu-id="c1a81-142">È possibile scaricare il [controllo Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) da MSDN.</span><span class="sxs-lookup"><span data-stu-id="c1a81-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="c1a81-143">Entrambe le versioni sono contenute nel download.</span><span class="sxs-lookup"><span data-stu-id="c1a81-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1a81-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1a81-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c1a81-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c1a81-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1a81-146">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c1a81-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="c1a81-147">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="c1a81-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 