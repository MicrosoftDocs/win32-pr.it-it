---
description: Le \_ costanti del flag di bit LINECALLPRIVILEGE descrivono i tipi di diritti di accesso o i privilegi che un'applicazione con un handle di chiamata potrebbe avere per la chiamata corrispondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Costanti LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332895"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="cc9bd-103">\_Costanti LINECALLPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="cc9bd-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="cc9bd-104">Le costanti del flag di bit **LINECALLPRIVILEGE \_** descrivono i tipi di diritti di accesso o i privilegi che un'applicazione con un handle di chiamata potrebbe avere per la chiamata corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="cc9bd-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_monitoraggio LINECALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="cc9bd-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc9bd-106">L'applicazione dispone di privilegi di monitoraggio per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="cc9bd-107">Questi privilegi consentono all'applicazione di monitorare le modifiche di stato e le informazioni di query e lo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc9bd-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ None**</span><span class="sxs-lookup"><span data-stu-id="cc9bd-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc9bd-109">L'applicazione non dispone di privilegi per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-109">The application has no privileges to the call.</span></span> <span data-ttu-id="cc9bd-110">L'handle dell'applicazione non è valido e non deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc9bd-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**\_proprietario LINECALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="cc9bd-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc9bd-112">L'applicazione dispone dei privilegi di proprietario per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="cc9bd-113">Questi privilegi consentono all'applicazione di modificare la chiamata in modi che influiscono sullo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc9bd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc9bd-114">Remarks</span></span>

<span data-ttu-id="cc9bd-115">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-115">No extensibility.</span></span> <span data-ttu-id="cc9bd-116">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="cc9bd-117">Quando un handle di chiamata viene fornito per la prima volta a un'applicazione o ogni volta che vengono modificati i privilegi di chiamata di tale applicazione, il messaggio di [**riga \_ CALLSTATE**](line-callstate.md) viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="cc9bd-118">Quando un'applicazione passa una chiamata e se l'applicazione ricevente non dispone già di un handle con privilegi di proprietario, questo messaggio informa l'applicazione sui nuovi privilegi della chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc9bd-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9bd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc9bd-119">Requirements</span></span>



| <span data-ttu-id="cc9bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc9bd-120">Requirement</span></span> | <span data-ttu-id="cc9bd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cc9bd-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc9bd-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="cc9bd-122">TAPI version</span></span><br/> | <span data-ttu-id="cc9bd-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cc9bd-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cc9bd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc9bd-124">Header</span></span><br/>       | <dl> <span data-ttu-id="cc9bd-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc9bd-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




