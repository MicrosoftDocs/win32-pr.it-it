---
title: Enumerazione WMDMMessage
description: Il tipo di enumerazione WMDMMessage definisce i tipi e gli Stati dei messaggi.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Enumerazione WMDMMessage Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325005"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="e5216-104">Enumerazione WMDMMessage</span><span class="sxs-lookup"><span data-stu-id="e5216-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="e5216-105">Il tipo di enumerazione **WMDMMessage** definisce i tipi e gli Stati dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="e5216-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5216-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5216-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="e5216-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="e5216-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5216-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_arrivo del \_ dispositivo \_ msg WMDM**</span><span class="sxs-lookup"><span data-stu-id="e5216-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5216-109">Un dispositivo Windows Media Gestione dispositivi è stato collegato.</span><span class="sxs-lookup"><span data-stu-id="e5216-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="e5216-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_rimozione del \_ dispositivo \_ msg WMDM**</span><span class="sxs-lookup"><span data-stu-id="e5216-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5216-111">Un dispositivo Windows Media Gestione dispositivi è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="e5216-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="e5216-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_arrivo del \_ supporto \_ messaggi WMDM**</span><span class="sxs-lookup"><span data-stu-id="e5216-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5216-113">Il supporto è stato inserito in un dispositivo Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5216-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="e5216-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_rimozione del \_ supporto \_ messaggi WMDM**</span><span class="sxs-lookup"><span data-stu-id="e5216-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5216-115">Il supporto è stato rimosso da un dispositivo Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5216-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5216-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5216-116">Requirements</span></span>



| <span data-ttu-id="e5216-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5216-117">Requirement</span></span> | <span data-ttu-id="e5216-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e5216-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5216-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5216-119">Header</span></span><br/> | <dl> <span data-ttu-id="e5216-120"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5216-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5216-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5216-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5216-122">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="e5216-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





