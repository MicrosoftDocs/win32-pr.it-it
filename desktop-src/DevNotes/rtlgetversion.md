---
description: Ottiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Funzione RtlGetVersion (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126405"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="67361-103">RtlGetVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="67361-103">RtlGetVersion function</span></span>

<span data-ttu-id="67361-104">Ottiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="67361-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="67361-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67361-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="67361-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67361-107">*lpVersionInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67361-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67361-108">Puntatore a una struttura [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una [**struttura \_ OSVERSIONINFOEXW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) che contiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="67361-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="67361-109">Un chiamante specifica quale struttura di input viene utilizzata impostando il membro **dwOSVersionInfoSize** della struttura sulla dimensione in byte della struttura utilizzata.</span><span class="sxs-lookup"><span data-stu-id="67361-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67361-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67361-110">Return value</span></span>

<span data-ttu-id="67361-111">Restituisce lo stato \_ riuscito.</span><span class="sxs-lookup"><span data-stu-id="67361-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="67361-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="67361-112">Remarks</span></span>

<span data-ttu-id="67361-113">**RtlGetVersion** è l'equivalente della funzione [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="67361-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="67361-114">Vedere l'esempio nell'Windows SDK che Mostra come ottenere la versione del sistema.</span><span class="sxs-lookup"><span data-stu-id="67361-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="67361-115">Quando si usa **RtlGetVersion** per determinare se una particolare versione del sistema operativo è in esecuzione, un chiamante deve verificare la presenza di numeri di versione maggiori o uguali al numero di versione richiesto.</span><span class="sxs-lookup"><span data-stu-id="67361-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="67361-116">In questo modo si garantisce la riuscita di un test della versione per le versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="67361-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="67361-117">Poiché è possibile aggiungere funzionalità del sistema operativo in una DLL ridistribuibile, controllare solo i numeri di versione principale e secondaria non è il modo più affidabile per verificare la presenza di una funzionalità di sistema specifica.</span><span class="sxs-lookup"><span data-stu-id="67361-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="67361-118">Un driver deve utilizzare [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) per verificare la presenza di una funzionalità di sistema specifica.</span><span class="sxs-lookup"><span data-stu-id="67361-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="67361-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67361-119">Requirements</span></span>



| <span data-ttu-id="67361-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67361-120">Requirement</span></span> | <span data-ttu-id="67361-121">Valore</span><span class="sxs-lookup"><span data-stu-id="67361-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67361-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67361-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67361-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="67361-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="67361-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67361-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67361-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="67361-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="67361-126">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="67361-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="67361-127"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="67361-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="67361-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67361-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="67361-129"><dt>Ntddk. h (include ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67361-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="67361-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="67361-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="67361-131"><dt>Ntdll. lib; </dt> <dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67361-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="67361-132">DLL</span><span class="sxs-lookup"><span data-stu-id="67361-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67361-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67361-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67361-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67361-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67361-135">**PsGetVersion**</span><span class="sxs-lookup"><span data-stu-id="67361-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
