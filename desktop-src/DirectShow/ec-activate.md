---
description: È in corso l'attivazione o la disattivazione di una finestra video.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328474"
---
# <a name="ec_activate"></a><span data-ttu-id="d0302-103">\_attivazione EC</span><span class="sxs-lookup"><span data-stu-id="d0302-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="d0302-104">È in corso l'attivazione o la disattivazione di una finestra video.</span><span class="sxs-lookup"><span data-stu-id="d0302-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0302-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0302-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0302-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d0302-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d0302-107">(**Bool**) **True** se la finestra è attivata oppure **false** se la finestra è disattivata.</span><span class="sxs-lookup"><span data-stu-id="d0302-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="d0302-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d0302-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d0302-109">(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer.</span><span class="sxs-lookup"><span data-stu-id="d0302-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d0302-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="d0302-110">Default Action</span></span>

<span data-ttu-id="d0302-111">Il gestore del grafico del filtro imposta lo stato attivo tramite l'interfaccia [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="d0302-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="d0302-112">Non invia la notifica degli eventi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0302-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0302-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0302-113">Remarks</span></span>

<span data-ttu-id="d0302-114">Un renderer video Invia questo evento ogni volta che la finestra viene attivata o disattivata, ovvero quando riceve un \_ messaggio ACTIVATEAPP WM.</span><span class="sxs-lookup"><span data-stu-id="d0302-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="d0302-115">L'attivazione o la disattivazione della finestra può verificarsi perché la finestra ha acquisito o perso lo stato attivo oppure perché il renderer è stato spostato tra la modalità a schermo intero e la modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="d0302-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="d0302-116">Questo evento consente a Filter Graph Manager di allocare risorse che dipendono dallo stato attivo della finestra, ad esempio i dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="d0302-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0302-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0302-117">Requirements</span></span>



| <span data-ttu-id="d0302-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0302-118">Requirement</span></span> | <span data-ttu-id="d0302-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d0302-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0302-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0302-120">Header</span></span><br/> | <dl> <span data-ttu-id="d0302-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0302-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0302-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0302-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0302-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="d0302-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d0302-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d0302-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




