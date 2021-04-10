---
description: Recupera la modalità protetta di Windows corrente. Windows può essere in modalità bloccata, in modalità normale o in modalità di valutazione.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Funzione WldpQueryWindowsLockdownMode (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225736"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="3161f-104">WldpQueryWindowsLockdownMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="3161f-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="3161f-105">Recupera la modalità protetta di Windows corrente.</span><span class="sxs-lookup"><span data-stu-id="3161f-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="3161f-106">Windows può essere in modalità bloccata, in modalità normale o in modalità di valutazione.</span><span class="sxs-lookup"><span data-stu-id="3161f-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3161f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3161f-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="3161f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3161f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3161f-109">*lockdownMode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3161f-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3161f-110">Se l'operazione riesce, restituisce una [**\_ modalità di \_ blocco \_ di Windows PWLDP**](wldp-windows-lockdown-mode.md) che indica la modalità protetta per il dispositivo Windows 10 corrente.</span><span class="sxs-lookup"><span data-stu-id="3161f-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3161f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3161f-111">Return value</span></span>

<span data-ttu-id="3161f-112">Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="3161f-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3161f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3161f-113">Requirements</span></span>



| <span data-ttu-id="3161f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3161f-114">Requirement</span></span> | <span data-ttu-id="3161f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3161f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3161f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3161f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3161f-117">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="3161f-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3161f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3161f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3161f-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3161f-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3161f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3161f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3161f-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3161f-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3161f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3161f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3161f-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3161f-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




