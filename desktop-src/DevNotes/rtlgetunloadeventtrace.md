---
description: Consente al codice di dump di ottenere le informazioni sul modulo non caricate da Ntdll.dll per l'archiviazione nel minidump.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330958"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="f3d8b-103">RtlGetUnloadEventTrace (funzione)</span><span class="sxs-lookup"><span data-stu-id="f3d8b-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="f3d8b-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="f3d8b-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="f3d8b-105">Consente al codice di dump di ottenere le informazioni sul modulo non caricate da Ntdll.dll per l'archiviazione nel minidump.</span><span class="sxs-lookup"><span data-stu-id="f3d8b-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d8b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3d8b-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="f3d8b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3d8b-107">Parameters</span></span>

<span data-ttu-id="f3d8b-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="f3d8b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3d8b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3d8b-109">Return value</span></span>

<span data-ttu-id="f3d8b-110">Questa funzione restituisce un puntatore a una matrice.</span><span class="sxs-lookup"><span data-stu-id="f3d8b-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="f3d8b-111">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f3d8b-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3d8b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3d8b-112">Remarks</span></span>

<span data-ttu-id="f3d8b-113">La matrice RtlpUnloadEventTrace è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="f3d8b-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="f3d8b-114">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f3d8b-114">This function has no associated header file.</span></span> <span data-ttu-id="f3d8b-115">La libreria di importazione associata, Ntdll. lib, è disponibile in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="f3d8b-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="f3d8b-116">È inoltre possibile chiamare questa funzione utilizzando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f3d8b-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d8b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3d8b-117">Requirements</span></span>



| <span data-ttu-id="f3d8b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d8b-118">Requirement</span></span> | <span data-ttu-id="f3d8b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f3d8b-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d8b-120">DLL</span></span><br/> | <dl> <span data-ttu-id="f3d8b-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3d8b-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
