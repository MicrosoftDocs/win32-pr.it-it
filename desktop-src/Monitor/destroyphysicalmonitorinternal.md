---
title: DestroyPhysicalMonitorInternal (funzione)
description: Chiude un handle a un monitor fisico.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Configurazione del monitoraggio della funzione DestroyPhysicalMonitorInternal
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873754"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="31af4-104">DestroyPhysicalMonitorInternal (funzione)</span><span class="sxs-lookup"><span data-stu-id="31af4-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31af4-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="31af4-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="31af4-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="31af4-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="31af4-107">Chiude un handle a un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="31af4-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="31af4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31af4-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="31af4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="31af4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31af4-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31af4-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31af4-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="31af4-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31af4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31af4-112">Return value</span></span>

<span data-ttu-id="31af4-113">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="31af4-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="31af4-114">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="31af4-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31af4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="31af4-115">Remarks</span></span>

<span data-ttu-id="31af4-116">Le applicazioni devono chiamare [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="31af4-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="31af4-117">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="31af4-117">This function has no associated import library.</span></span> <span data-ttu-id="31af4-118">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="31af4-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="31af4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31af4-119">Requirements</span></span>



| <span data-ttu-id="31af4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="31af4-120">Requirement</span></span> | <span data-ttu-id="31af4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="31af4-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31af4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31af4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31af4-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31af4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="31af4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31af4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31af4-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31af4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31af4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="31af4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31af4-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31af4-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31af4-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31af4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31af4-129">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="31af4-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

