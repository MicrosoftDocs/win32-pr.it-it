---
description: È in corso l'arresto del grafico del filtro prima di essere eliminato definitivamente.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327187"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="0165f-103">\_arresto di EC \_</span><span class="sxs-lookup"><span data-stu-id="0165f-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="0165f-104">È in corso l'arresto del grafico del filtro prima di essere eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="0165f-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="0165f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0165f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0165f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0165f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0165f-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="0165f-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="0165f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0165f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0165f-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="0165f-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0165f-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="0165f-110">Default Action</span></span>

<span data-ttu-id="0165f-111">Questo evento non viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0165f-111">This event is not sent to the application.</span></span> <span data-ttu-id="0165f-112">Il gestore del grafo del filtro lo invia ai distributori plug-in per notificare che il grafico è in fase di chiusura.</span><span class="sxs-lookup"><span data-stu-id="0165f-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="0165f-113">Le applicazioni non possono eseguire l'override dell'azione predefinita di questo evento.</span><span class="sxs-lookup"><span data-stu-id="0165f-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0165f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0165f-114">Requirements</span></span>



| <span data-ttu-id="0165f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0165f-115">Requirement</span></span> | <span data-ttu-id="0165f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0165f-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0165f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0165f-117">Header</span></span><br/> | <dl> <span data-ttu-id="0165f-118"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0165f-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0165f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0165f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0165f-120">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="0165f-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0165f-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0165f-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




