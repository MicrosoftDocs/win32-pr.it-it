---
description: Identifica il tipo di host del chiamante WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Enumerazione WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522922"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="b1552-103">\_ \_ Enumerazione ID host WLDP</span><span class="sxs-lookup"><span data-stu-id="b1552-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="b1552-104">Identifica il tipo di host del chiamante WLDP.</span><span class="sxs-lookup"><span data-stu-id="b1552-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1552-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1552-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="b1552-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b1552-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1552-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ \_ID host \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="b1552-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="b1552-108">Il tipo di host è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b1552-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_ID host \_ globale**</span><span class="sxs-lookup"><span data-stu-id="b1552-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-110">Il tipo di host è criteri globali.</span><span class="sxs-lookup"><span data-stu-id="b1552-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**\_ID host \_ WLDP \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="b1552-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-112">Il tipo di host è VBScript.</span><span class="sxs-lookup"><span data-stu-id="b1552-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_ID host \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="b1552-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-114">Il tipo di host è Windows script host.</span><span class="sxs-lookup"><span data-stu-id="b1552-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_ID host \_ PowerShell**</span><span class="sxs-lookup"><span data-stu-id="b1552-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-116">Il tipo di host è Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1552-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_ID host \_ IE**</span><span class="sxs-lookup"><span data-stu-id="b1552-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-118">Il tipo di host è Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b1552-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_ID host \_ MSI**</span><span class="sxs-lookup"><span data-stu-id="b1552-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="b1552-120">Il tipo di host è il Microsoft Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b1552-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="b1552-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ID host \_ Max**</span><span class="sxs-lookup"><span data-stu-id="b1552-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="b1552-122">Valore massimo dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="b1552-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1552-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1552-123">Requirements</span></span>



| <span data-ttu-id="b1552-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1552-124">Requirement</span></span> | <span data-ttu-id="b1552-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b1552-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b1552-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1552-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b1552-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b1552-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1552-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1552-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b1552-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b1552-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b1552-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1552-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1552-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1552-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




