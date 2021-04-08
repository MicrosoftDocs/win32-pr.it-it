---
title: GetNumberOfPhysicalMonitors (funzione)
description: Ottiene il numero di monitoraggi phyical associati a un dispositivo di visualizzazione.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configurazione del monitoraggio della funzione GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873753"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="67afe-104">GetNumberOfPhysicalMonitors (funzione)</span><span class="sxs-lookup"><span data-stu-id="67afe-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67afe-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67afe-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="67afe-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="67afe-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="67afe-107">Ottiene il numero di monitoraggi phyical associati a un dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67afe-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="67afe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67afe-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="67afe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="67afe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67afe-110">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67afe-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67afe-111">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="67afe-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="67afe-112">*pdwNumberOfPhysicalMonitors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67afe-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67afe-113">Riceve il numero di monitoraggi fisici.</span><span class="sxs-lookup"><span data-stu-id="67afe-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67afe-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67afe-114">Return value</span></span>

<span data-ttu-id="67afe-115">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="67afe-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="67afe-116">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="67afe-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67afe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="67afe-117">Remarks</span></span>

<span data-ttu-id="67afe-118">Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="67afe-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="67afe-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="67afe-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="67afe-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="67afe-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="67afe-121">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="67afe-121">This function has no associated import library.</span></span> <span data-ttu-id="67afe-122">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="67afe-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="67afe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67afe-123">Requirements</span></span>



| <span data-ttu-id="67afe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="67afe-124">Requirement</span></span> | <span data-ttu-id="67afe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="67afe-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67afe-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67afe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="67afe-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67afe-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="67afe-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67afe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="67afe-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67afe-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="67afe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="67afe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67afe-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67afe-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67afe-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67afe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67afe-133">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="67afe-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

