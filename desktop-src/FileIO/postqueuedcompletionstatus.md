---
description: Invia un pacchetto di completamento di I/O a una porta di completamento di I/O.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Funzione PostQueuedCompletionStatus ha provocato (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316285"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="153f4-103">PostQueuedCompletionStatus ha provocato (funzione)</span><span class="sxs-lookup"><span data-stu-id="153f4-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="153f4-104">Invia un pacchetto di completamento di I/O a una porta di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="153f4-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="153f4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="153f4-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="153f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="153f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153f4-107">*Tentato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="153f4-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-108">Handle per una porta di completamento di I/O a cui deve essere inviato il pacchetto di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="153f4-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-109">*dwNumberOfBytesTransferred* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="153f4-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-110">Valore da restituire tramite il parametro *lpNumberOfBytesTransferred* della funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="153f4-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-111">*dwCompletionKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="153f4-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-112">Valore da restituire tramite il parametro *lpCompletionKey* della funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="153f4-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="153f4-113">*lpOverlapped* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="153f4-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="153f4-114">Valore da restituire tramite il parametro *lpOverlapped* della funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="153f4-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153f4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="153f4-115">Return value</span></span>

<span data-ttu-id="153f4-116">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="153f4-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="153f4-117">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="153f4-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="153f4-118">Per ottenere informazioni estese sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="153f4-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="153f4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="153f4-119">Remarks</span></span>

<span data-ttu-id="153f4-120">Il pacchetto di completamento I/O soddisferà una chiamata in attesa alla funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="153f4-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="153f4-121">Questa funzione restituisce con i tre valori passati come secondo, terzo e quarto parametro della chiamata a **PostQueuedCompletionStatus ha provocato**.</span><span class="sxs-lookup"><span data-stu-id="153f4-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="153f4-122">Il sistema non utilizza né convalida questi valori.</span><span class="sxs-lookup"><span data-stu-id="153f4-122">The system does not use or validate these values.</span></span> <span data-ttu-id="153f4-123">In particolare, il parametro *lpOverlapped* non deve puntare a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="153f4-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="153f4-124">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="153f4-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="153f4-125">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="153f4-125">Technology</span></span>                                           | <span data-ttu-id="153f4-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="153f4-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="153f4-127">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="153f4-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="153f4-128">Sì</span><span class="sxs-lookup"><span data-stu-id="153f4-128">Yes</span></span><br/> |
| <span data-ttu-id="153f4-129">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="153f4-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="153f4-130">Sì</span><span class="sxs-lookup"><span data-stu-id="153f4-130">Yes</span></span><br/> |
| <span data-ttu-id="153f4-131">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="153f4-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="153f4-132">Sì</span><span class="sxs-lookup"><span data-stu-id="153f4-132">Yes</span></span><br/> |
| <span data-ttu-id="153f4-133">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="153f4-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="153f4-134">Sì</span><span class="sxs-lookup"><span data-stu-id="153f4-134">Yes</span></span><br/> |
| <span data-ttu-id="153f4-135">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="153f4-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="153f4-136">Sì</span><span class="sxs-lookup"><span data-stu-id="153f4-136">Yes</span></span><br/> |



 

<span data-ttu-id="153f4-137">CsvFs eseguirà l'i/o reindirizzato per i file compressi.</span><span class="sxs-lookup"><span data-stu-id="153f4-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="153f4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="153f4-138">Requirements</span></span>



| <span data-ttu-id="153f4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="153f4-139">Requirement</span></span> | <span data-ttu-id="153f4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="153f4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153f4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="153f4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="153f4-142">App desktop di Windows XP \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="153f4-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="153f4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="153f4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="153f4-144">App UWP per \[ app desktop di Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="153f4-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="153f4-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="153f4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="153f4-146"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="153f4-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="153f4-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="153f4-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="153f4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="153f4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153f4-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153f4-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="153f4-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="153f4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153f4-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="153f4-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="153f4-153">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="153f4-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="153f4-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="153f4-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="153f4-155">**OVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="153f4-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

