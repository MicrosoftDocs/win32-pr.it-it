---
description: Descrive le modalità protette per un dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumerazione WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332366"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="70c98-103">\_Enumerazione della \_ modalità di blocco di Windows WLDP \_</span><span class="sxs-lookup"><span data-stu-id="70c98-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="70c98-104">Descrive le modalità protette per un dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="70c98-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="70c98-105">Usato principalmente in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span><span class="sxs-lookup"><span data-stu-id="70c98-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70c98-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70c98-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="70c98-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="70c98-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="70c98-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modalità di blocco di Windows WLDP \_ \_ \_ sbloccata**</span><span class="sxs-lookup"><span data-stu-id="70c98-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="70c98-109">Sbloccato.</span><span class="sxs-lookup"><span data-stu-id="70c98-109">Unlocked.</span></span> <span data-ttu-id="70c98-110">Usato principalmente per i dispositivi Windows senza la modalità S.</span><span class="sxs-lookup"><span data-stu-id="70c98-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="70c98-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**versione di valutazione di WLDP \_ Windows \_ Lockdown \_ mode \_**</span><span class="sxs-lookup"><span data-stu-id="70c98-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="70c98-112">Valutazione.</span><span class="sxs-lookup"><span data-stu-id="70c98-112">Trial.</span></span> <span data-ttu-id="70c98-113">Usato principalmente per un dispositivo di valutazione Windows 10 con la modalità S.</span><span class="sxs-lookup"><span data-stu-id="70c98-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="70c98-114">La modalità di valutazione è un caso speciale per i dispositivi Windows 10 con la modalità S: i criteri vengono applicati, ma non esiste alcuna protezione anti-rollback per l'applicazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="70c98-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="70c98-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**\_modalità di blocco di Windows WLDP \_ \_ \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="70c98-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="70c98-116">Bloccato.</span><span class="sxs-lookup"><span data-stu-id="70c98-116">Locked.</span></span> <span data-ttu-id="70c98-117">Usato principalmente per un dispositivo Windows 10 con la modalità S.</span><span class="sxs-lookup"><span data-stu-id="70c98-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="70c98-118">Un dispositivo bloccato imporrà i criteri di Device Guard firmati forniti con l'immagine del sistema operativo Windows 10 con la modalità S.</span><span class="sxs-lookup"><span data-stu-id="70c98-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="70c98-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ \_ modalità blocco \_ Windows \_ Max**</span><span class="sxs-lookup"><span data-stu-id="70c98-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="70c98-120">Valore massimo dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="70c98-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70c98-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70c98-121">Requirements</span></span>



| <span data-ttu-id="70c98-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c98-122">Requirement</span></span> | <span data-ttu-id="70c98-123">Valore</span><span class="sxs-lookup"><span data-stu-id="70c98-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="70c98-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70c98-124">Header</span></span><br/> | <dl> <span data-ttu-id="70c98-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c98-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




