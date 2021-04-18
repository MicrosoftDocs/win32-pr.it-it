---
title: Enumerazione WMDM_SESSION_TYPE
description: Il tipo di \_ enumerazione del tipo di sessione WMDM \_ definisce il tipo di sessione.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Enumerazione WMDM_SESSION_TYPE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325271"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="447cb-104">Enumerazione del tipo di \_ sessione WMDM \_</span><span class="sxs-lookup"><span data-stu-id="447cb-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="447cb-105">Il tipo di enumerazione del **\_ \_ tipo di sessione WMDM** definisce il tipo di sessione.</span><span class="sxs-lookup"><span data-stu-id="447cb-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="447cb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="447cb-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="447cb-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="447cb-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="447cb-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ sessione \_ None**</span><span class="sxs-lookup"><span data-stu-id="447cb-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="447cb-109">La sessione non è definita.</span><span class="sxs-lookup"><span data-stu-id="447cb-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="447cb-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_trasferimento della sessione WMDM \_ \_ al \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="447cb-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="447cb-111">La sessione viene definita come trasferimento dei dati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="447cb-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="447cb-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ trasferimento della sessione WMDM \_ dal \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="447cb-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="447cb-113">La sessione viene definita come trasferimento dei dati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="447cb-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="447cb-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_eliminazione della sessione WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="447cb-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="447cb-115">La sessione è definita come eliminazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="447cb-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="447cb-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_personalizzata della sessione WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="447cb-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="447cb-117">La sessione viene definita come sessione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="447cb-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="447cb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="447cb-118">Requirements</span></span>



| <span data-ttu-id="447cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="447cb-119">Requirement</span></span> | <span data-ttu-id="447cb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="447cb-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="447cb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="447cb-121">Header</span></span><br/> | <dl> <span data-ttu-id="447cb-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="447cb-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="447cb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="447cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447cb-124">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="447cb-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





