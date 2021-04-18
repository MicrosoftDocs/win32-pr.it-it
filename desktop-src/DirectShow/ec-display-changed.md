---
description: La modalità di visualizzazione è cambiata.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331114"
---
# <a name="ec_display_changed"></a><span data-ttu-id="4cf46-103">visualizzazione di EC \_ \_ modificata</span><span class="sxs-lookup"><span data-stu-id="4cf46-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="4cf46-104">La modalità di visualizzazione è cambiata.</span><span class="sxs-lookup"><span data-stu-id="4cf46-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cf46-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cf46-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf46-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4cf46-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4cf46-107">(**IUnknown** \* ) Puntatore a una matrice di interfacce [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) per i pin di input del renderer video.</span><span class="sxs-lookup"><span data-stu-id="4cf46-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="4cf46-108">Se *lParam2* è zero, questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf46-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf46-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4cf46-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4cf46-110">Se *lParam2* è zero, *lParam1* contiene un solo puntatore **Ipin** o è uguale a **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf46-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="4cf46-111">Se *lParam2* è maggiore di zero, *lParam1* contiene una matrice di puntatori **Ipin** e il numero di elementi nella matrice viene fornito da *lParam2*.</span><span class="sxs-lookup"><span data-stu-id="4cf46-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4cf46-112">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="4cf46-112">Default Action</span></span>

<span data-ttu-id="4cf46-113">Filter Graph Manager Arresta temporaneamente il grafo, quindi disconnette e riconnette il renderer video.</span><span class="sxs-lookup"><span data-stu-id="4cf46-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="4cf46-114">L'evento non viene passato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cf46-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf46-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cf46-115">Remarks</span></span>

<span data-ttu-id="4cf46-116">I renderer video possono inviare questo evento in risposta a un messaggio [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="4cf46-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="4cf46-117">Il messaggio **WM \_ DISPLAYCHANGE** indica che l'utente ha modificato la risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4cf46-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="4cf46-118">Durante la connessione pin, la maggior parte dei renderer video sceglie un formato basato sulla modalità di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4cf46-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="4cf46-119">Se la modalità di visualizzazione cambia, il renderer video potrebbe dover scegliere un altro formato.</span><span class="sxs-lookup"><span data-stu-id="4cf46-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="4cf46-120">Inviando questo messaggio, il renderer segnala al gestore del grafico dei filtri che è necessario riconnetterlo.</span><span class="sxs-lookup"><span data-stu-id="4cf46-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="4cf46-121">Durante la riconnessione, il renderer può selezionare un nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="4cf46-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="4cf46-122">Se la riconnessione ha esito negativo, il gestore del grafico dei filtri Invia un evento [**\_ ERRORABORT EC**](ec-errorabort.md) all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cf46-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="4cf46-123">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="4cf46-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="4cf46-124">Un presentatore personalizzato per il [**renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR) deve inviare questo evento al EVR se il dispositivo Direct3D del Presenter viene modificato.</span><span class="sxs-lookup"><span data-stu-id="4cf46-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="4cf46-125">Impostare *lParam1* e *lParam2* su zero; EVR ignora i parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4cf46-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf46-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cf46-126">Requirements</span></span>



| <span data-ttu-id="4cf46-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf46-127">Requirement</span></span> | <span data-ttu-id="4cf46-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4cf46-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf46-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cf46-129">Header</span></span><br/> | <dl> <span data-ttu-id="4cf46-130"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf46-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf46-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cf46-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf46-132">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="4cf46-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4cf46-133">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cf46-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

