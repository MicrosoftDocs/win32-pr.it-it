---
title: DDCCIGetCapabilitiesStringLength (funzione)
description: Ottiene la lunghezza di una stringa di funzionalità per un monitoraggio.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301269"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="bf629-104">DDCCIGetCapabilitiesStringLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="bf629-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf629-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bf629-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="bf629-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="bf629-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="bf629-107">Ottiene la lunghezza di una stringa di funzionalità per un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bf629-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf629-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf629-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="bf629-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf629-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf629-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf629-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf629-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="bf629-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="bf629-112">*pdwLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf629-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf629-113">Riceve la lunghezza della stringa di funzionalità, in caratteri, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="bf629-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf629-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf629-114">Return value</span></span>

<span data-ttu-id="bf629-115">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="bf629-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="bf629-116">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="bf629-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf629-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf629-117">Remarks</span></span>

<span data-ttu-id="bf629-118">Le applicazioni devono chiamare [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="bf629-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="bf629-119">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="bf629-119">This function has no associated import library.</span></span> <span data-ttu-id="bf629-120">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="bf629-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf629-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf629-121">Requirements</span></span>



| <span data-ttu-id="bf629-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf629-122">Requirement</span></span> | <span data-ttu-id="bf629-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bf629-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf629-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf629-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf629-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf629-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bf629-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf629-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf629-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf629-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf629-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bf629-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf629-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf629-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf629-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf629-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf629-131">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="bf629-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

