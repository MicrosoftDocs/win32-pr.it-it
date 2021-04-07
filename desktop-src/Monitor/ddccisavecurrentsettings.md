---
title: DDCCISaveCurrentSettings (funzione)
description: Salva le impostazioni di monitoraggio correnti nell'archiviazione non volatile dello schermo.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Configurazione del monitoraggio della funzione DDCCISaveCurrentSettings
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964021"
---
# <a name="ddccisavecurrentsettings-function"></a><span data-ttu-id="907d6-104">DDCCISaveCurrentSettings (funzione)</span><span class="sxs-lookup"><span data-stu-id="907d6-104">DDCCISaveCurrentSettings function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="907d6-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="907d6-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="907d6-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="907d6-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="907d6-107">Salva le impostazioni di monitoraggio correnti nell'archiviazione non volatile dello schermo.</span><span class="sxs-lookup"><span data-stu-id="907d6-107">Saves the current monitor settings to the display's nonvolatile storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="907d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="907d6-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="907d6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="907d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907d6-110">*hMonitor*</span><span class="sxs-lookup"><span data-stu-id="907d6-110">*hMonitor*</span></span> 
</dt> <dd>

<span data-ttu-id="907d6-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="907d6-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="907d6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="907d6-112">Return value</span></span>

<span data-ttu-id="907d6-113">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="907d6-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="907d6-114">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="907d6-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="907d6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="907d6-115">Remarks</span></span>

<span data-ttu-id="907d6-116">Le applicazioni devono chiamare [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="907d6-116">Applications should call [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) instead of calling this function.</span></span>

<span data-ttu-id="907d6-117">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="907d6-117">This function has no associated import library.</span></span> <span data-ttu-id="907d6-118">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="907d6-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="907d6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="907d6-119">Requirements</span></span>



| <span data-ttu-id="907d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="907d6-120">Requirement</span></span> | <span data-ttu-id="907d6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="907d6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="907d6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="907d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="907d6-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="907d6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="907d6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="907d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="907d6-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="907d6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="907d6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="907d6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="907d6-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="907d6-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="907d6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="907d6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907d6-129">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="907d6-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

