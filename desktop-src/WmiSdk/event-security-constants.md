---
description: Di seguito vengono illustrate le costanti di sicurezza WMI utilizzate per gli eventi. Vengono usati per impostare le voci di controllo di accesso (ACE) nei descrittori di sicurezza usati per eventi o sink.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Costanti di sicurezza degli eventi (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131155"
---
# <a name="event-security-constants"></a><span data-ttu-id="1e67c-104">Costanti di sicurezza degli eventi</span><span class="sxs-lookup"><span data-stu-id="1e67c-104">Event Security Constants</span></span>

<span data-ttu-id="1e67c-105">Di seguito vengono illustrate le costanti di sicurezza WMI utilizzate per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1e67c-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="1e67c-106">Vengono usati per impostare le voci di controllo di accesso (ACE) nei descrittori di sicurezza usati per eventi o sink.</span><span class="sxs-lookup"><span data-stu-id="1e67c-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="1e67c-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_pubblicazione con diritto WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="1e67c-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e67c-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="1e67c-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="1e67c-109">Specifica che l'account può pubblicare eventi nell'istanza di [**\_ \_ EventFilter**](--eventfilter.md) che definisce il filtro eventi per un consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="1e67c-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="1e67c-110">Disponibile in wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="1e67c-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e67c-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_sottoscrizione a destra di WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="1e67c-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e67c-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="1e67c-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="1e67c-113">Specifica che un consumer può sottoscrivere gli eventi recapitati a un sink.</span><span class="sxs-lookup"><span data-stu-id="1e67c-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="1e67c-114">Usato in [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span><span class="sxs-lookup"><span data-stu-id="1e67c-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="1e67c-115">Disponibile in wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="1e67c-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e67c-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ soggetto \_ a \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="1e67c-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e67c-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="1e67c-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="1e67c-118">Il provider di eventi indica che WMI controlla la proprietà del **\_ descrittore di sicurezza** in ogni evento (ereditato dall' [**\_ \_ evento**](--event.md)) e invia solo gli eventi agli utenti con le autorizzazioni di accesso appropriate.</span><span class="sxs-lookup"><span data-stu-id="1e67c-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="1e67c-119">Disponibile in wbemprov. h.</span><span class="sxs-lookup"><span data-stu-id="1e67c-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e67c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e67c-120">Requirements</span></span>



| <span data-ttu-id="1e67c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e67c-121">Requirement</span></span> | <span data-ttu-id="1e67c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1e67c-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e67c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e67c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e67c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e67c-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="1e67c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e67c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e67c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e67c-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="1e67c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e67c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e67c-128"><dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e67c-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e67c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e67c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e67c-130">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="1e67c-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="1e67c-131">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="1e67c-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="1e67c-132">Protezione degli eventi WMI</span><span class="sxs-lookup"><span data-stu-id="1e67c-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




