---
title: GetPhysicalMonitors (funzione)
description: Ottiene i monitoraggi fisici associati a un dispositivo di visualizzazione.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configurazione del monitoraggio della funzione GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301584"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="2aebc-104">GetPhysicalMonitors (funzione)</span><span class="sxs-lookup"><span data-stu-id="2aebc-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aebc-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2aebc-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="2aebc-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2aebc-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="2aebc-107">Ottiene i monitoraggi fisici associati a un dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2aebc-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aebc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aebc-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="2aebc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2aebc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aebc-110">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aebc-111">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2aebc-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="2aebc-112">*dwPhysicalMonitorArraySize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aebc-113">Numero di elementi nella matrice *pdwNumPhysicalMonitorHandlesInArray* .</span><span class="sxs-lookup"><span data-stu-id="2aebc-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="2aebc-114">Per ottenere le dimensioni richieste della matrice, chiamare [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="2aebc-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="2aebc-115">*pdwNumPhysicalMonitorHandlesInArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aebc-116">Riceve il numero di elementi che la funzione copia nella matrice *phPhysicalMonitorArray* .</span><span class="sxs-lookup"><span data-stu-id="2aebc-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="2aebc-117">*phPhysicalMonitorArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aebc-118">Matrice che riceve handle per i monitoraggi fisici.</span><span class="sxs-lookup"><span data-stu-id="2aebc-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="2aebc-119">Ogni handle deve essere rilasciato chiamando [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span><span class="sxs-lookup"><span data-stu-id="2aebc-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aebc-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2aebc-120">Return value</span></span>

<span data-ttu-id="2aebc-121">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="2aebc-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="2aebc-122">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="2aebc-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aebc-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2aebc-123">Remarks</span></span>

<span data-ttu-id="2aebc-124">Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2aebc-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="2aebc-125">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="2aebc-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="2aebc-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="2aebc-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="2aebc-127">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="2aebc-127">This function has no associated import library.</span></span> <span data-ttu-id="2aebc-128">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="2aebc-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aebc-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2aebc-129">Requirements</span></span>



| <span data-ttu-id="2aebc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aebc-130">Requirement</span></span> | <span data-ttu-id="2aebc-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2aebc-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2aebc-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aebc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2aebc-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2aebc-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aebc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2aebc-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2aebc-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2aebc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2aebc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aebc-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aebc-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aebc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2aebc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aebc-139">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="2aebc-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

