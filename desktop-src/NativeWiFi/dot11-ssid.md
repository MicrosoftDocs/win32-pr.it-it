---
description: Contiene l'SSID di un'interfaccia.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Struttura DOT11_SSID (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882677"
---
# <a name="dot11_ssid-structure"></a><span data-ttu-id="7a4a0-103">\_Struttura SSID DOT11</span><span class="sxs-lookup"><span data-stu-id="7a4a0-103">DOT11\_SSID structure</span></span>

<span data-ttu-id="7a4a0-104">Una **struttura \_ SSID DOT11** contiene il valore SSID di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-104">A **DOT11\_SSID** structure contains the SSID of an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a4a0-105">Syntax</span></span>


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a><span data-ttu-id="7a4a0-106">Members</span><span class="sxs-lookup"><span data-stu-id="7a4a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a4a0-107">**uSSIDLength**</span><span class="sxs-lookup"><span data-stu-id="7a4a0-107">**uSSIDLength**</span></span>
</dt> <dd>

<span data-ttu-id="7a4a0-108">Lunghezza, in byte, della matrice **ucSSID** .</span><span class="sxs-lookup"><span data-stu-id="7a4a0-108">The length, in bytes, of the **ucSSID** array.</span></span>

</dd> <dt>

<span data-ttu-id="7a4a0-109">**ucSSID**</span><span class="sxs-lookup"><span data-stu-id="7a4a0-109">**ucSSID**</span></span>
</dt> <dd>

<span data-ttu-id="7a4a0-110">SSID.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-110">The SSID.</span></span> <span data-ttu-id="7a4a0-111">\_ \_ La lunghezza massima SSID DOT11 \_ è impostata su 32.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-111">DOT11\_SSID\_MAX\_LENGTH is set to 32.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a4a0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a4a0-112">Remarks</span></span>

<span data-ttu-id="7a4a0-113">L'SSID specificato dal membro **ucSSID** non è una stringa ASCII con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-113">The SSID that is specified by the **ucSSID** member is not a null-terminated ASCII string.</span></span> <span data-ttu-id="7a4a0-114">La lunghezza del SSID è determinata dal membro **uSSIDLength** .</span><span class="sxs-lookup"><span data-stu-id="7a4a0-114">The length of the SSID is determined by the **uSSIDLength** member.</span></span>

<span data-ttu-id="7a4a0-115">Un SSID con caratteri jolly è un SSID il cui membro **uSSIDLength** è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-115">A wildcard SSID is an SSID whose **uSSIDLength** member is set to zero.</span></span> <span data-ttu-id="7a4a0-116">Quando l'SSID desiderato è impostato sull'SSID con caratteri jolly, la stazione 802,11 può connettersi a qualsiasi rete di Service Set (BSS) di base.</span><span class="sxs-lookup"><span data-stu-id="7a4a0-116">When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4a0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a4a0-117">Requirements</span></span>



| <span data-ttu-id="7a4a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a4a0-118">Requirement</span></span> | <span data-ttu-id="7a4a0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7a4a0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4a0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a4a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4a0-121">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="7a4a0-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7a4a0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a4a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4a0-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a4a0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="7a4a0-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7a4a0-124">Redistributable</span></span><br/>          | <span data-ttu-id="7a4a0-125">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="7a4a0-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="7a4a0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a4a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4a0-127"><dt>Wlantypes. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a4a0-127"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4a0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a4a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4a0-129">**\_parametri di connessione WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="7a4a0-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="7a4a0-130">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="7a4a0-130">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[<span data-ttu-id="7a4a0-131">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="7a4a0-131">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




