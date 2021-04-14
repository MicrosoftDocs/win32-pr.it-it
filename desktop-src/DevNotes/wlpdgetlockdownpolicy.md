---
description: Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e lo script o l'identità del servizio gestito da usare.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Funzione WldpGetLockdownPolicy (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523465"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="ba95a-103">WldpGetLockdownPolicy (funzione)</span><span class="sxs-lookup"><span data-stu-id="ba95a-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="ba95a-104">Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e lo script o l'identità del servizio gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="ba95a-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="ba95a-105">Alla funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="ba95a-105">The function has no associated import library.</span></span> <span data-ttu-id="ba95a-106">È necessario utilizzare le funzioni LoadLibrary e GetProcAddress per collegare dinamicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="ba95a-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba95a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba95a-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ba95a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba95a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba95a-109">*hostInformation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ba95a-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba95a-110">Struttura [**di \_ \_ informazioni sull'host WLDP**](wldp-host-information.md) che identifica l'host e il file di origine da valutare.</span><span class="sxs-lookup"><span data-stu-id="ba95a-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="ba95a-111">*lockdownState* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ba95a-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba95a-112">Fornisce il valore sicuro del criterio risultante.</span><span class="sxs-lookup"><span data-stu-id="ba95a-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="ba95a-113">Se! WLDP_LOCKDOWN_IS_OFF, UMCI è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ba95a-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="ba95a-114">È inoltre possibile controllare WLDP_LOCKDOWN_IS_AUDIT e WLDP_LOCKDOWN_IS_ENFORCE per determinare se un criterio è in modalità di controllo o di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba95a-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="ba95a-115">*lockdownFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba95a-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba95a-116">I valori di flag seguenti sono definiti WLDP \_ flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – When set, Skip the SaferIdentifyLevel Validation, che ignorerà se uno script è firmato.</span><span class="sxs-lookup"><span data-stu-id="ba95a-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba95a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba95a-117">Return value</span></span>

<span data-ttu-id="ba95a-118">Questo metodo restituisce \_ OK se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="ba95a-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba95a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba95a-119">Remarks</span></span>

<span data-ttu-id="ba95a-120">Quando viene chiamato con \_ \_ le informazioni sull'host WLDP. SZSOURCE = null, vengono restituiti i criteri generici per l'host.</span><span class="sxs-lookup"><span data-stu-id="ba95a-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="ba95a-121">Quando viene chiamato con \_ le \_ informazioni sull'host WLDP. DWHOSTID = WLDP \_ \_ ID host \_ globale, WLDP \_ host \_ Information. szSource deve essere null e la funzione restituirà i criteri di sistema globali.</span><span class="sxs-lookup"><span data-stu-id="ba95a-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="ba95a-122">I flag dwFlag \_ WLDP \_ SKIPSIGNATUREVALIDATION possono essere usati per ignorare la convalida SaferIdentifyLevel (), che ignorerà se uno script è firmato.</span><span class="sxs-lookup"><span data-stu-id="ba95a-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba95a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba95a-123">Requirements</span></span>



| <span data-ttu-id="ba95a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba95a-124">Requirement</span></span> | <span data-ttu-id="ba95a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ba95a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba95a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba95a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba95a-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ba95a-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ba95a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba95a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba95a-129">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ba95a-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba95a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba95a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba95a-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba95a-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba95a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ba95a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba95a-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba95a-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




