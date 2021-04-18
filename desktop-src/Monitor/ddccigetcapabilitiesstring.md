---
title: DDCCIGetCapabilitiesString (funzione)
description: Ottiene una stringa che descrive le funzionalità di un monitoraggio.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301586"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="0430f-104">DDCCIGetCapabilitiesString (funzione)</span><span class="sxs-lookup"><span data-stu-id="0430f-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0430f-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0430f-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="0430f-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0430f-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="0430f-107">Ottiene una stringa che descrive le funzionalità di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0430f-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0430f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0430f-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="0430f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0430f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0430f-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0430f-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0430f-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="0430f-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="0430f-112">*pszString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0430f-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0430f-113">Puntatore a un buffer che riceve la stringa di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0430f-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="0430f-114">Per ottenere la lunghezza della stringa delle funzionalità, chiamare [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="0430f-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="0430f-115">*dwLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0430f-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0430f-116">Dimensioni del buffer *pszString* , in caratteri, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="0430f-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0430f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0430f-117">Return value</span></span>

<span data-ttu-id="0430f-118">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="0430f-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="0430f-119">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="0430f-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0430f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0430f-120">Remarks</span></span>

<span data-ttu-id="0430f-121">Le applicazioni devono chiamare [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0430f-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="0430f-122">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="0430f-122">This function has no associated import library.</span></span> <span data-ttu-id="0430f-123">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="0430f-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0430f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0430f-124">Requirements</span></span>



| <span data-ttu-id="0430f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0430f-125">Requirement</span></span> | <span data-ttu-id="0430f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0430f-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0430f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0430f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0430f-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0430f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0430f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0430f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0430f-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0430f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0430f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0430f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0430f-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0430f-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0430f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0430f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0430f-134">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="0430f-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

