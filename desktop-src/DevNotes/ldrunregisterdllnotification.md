---
description: Annulla la notifica di caricamento DLL precedentemente registrata chiamando la funzione LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401360"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="d47d0-103">LdrUnregisterDllNotification (funzione)</span><span class="sxs-lookup"><span data-stu-id="d47d0-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="d47d0-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="d47d0-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="d47d0-105">Annulla la notifica di caricamento DLL precedentemente registrata chiamando la funzione [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d47d0-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47d0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d47d0-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="d47d0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d47d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47d0-108">*Cookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d47d0-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47d0-109">Puntatore all'identificatore di callback ricevuto dalla chiamata [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) registrata per la notifica.</span><span class="sxs-lookup"><span data-stu-id="d47d0-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47d0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d47d0-110">Return value</span></span>

<span data-ttu-id="d47d0-111">Restituisce un codice **NTSTATUS** o Error.</span><span class="sxs-lookup"><span data-stu-id="d47d0-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="d47d0-112">Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="d47d0-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="d47d0-113">Se la funzione di callback non viene trovata, la funzione restituisce la **dll di stato \_ \_ non \_ trovata**.</span><span class="sxs-lookup"><span data-stu-id="d47d0-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="d47d0-114">I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.</span><span class="sxs-lookup"><span data-stu-id="d47d0-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d47d0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d47d0-115">Remarks</span></span>

<span data-ttu-id="d47d0-116">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d47d0-116">This function has no associated header file.</span></span> <span data-ttu-id="d47d0-117">La libreria di importazione associata, Ntdll. lib, è disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="d47d0-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="d47d0-118">È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="d47d0-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47d0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d47d0-119">Requirements</span></span>



| <span data-ttu-id="d47d0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d47d0-120">Requirement</span></span> | <span data-ttu-id="d47d0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d47d0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d47d0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d47d0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d47d0-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d47d0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d47d0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d47d0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d47d0-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d47d0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d47d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d47d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d47d0-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47d0-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47d0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d47d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47d0-129">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="d47d0-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
