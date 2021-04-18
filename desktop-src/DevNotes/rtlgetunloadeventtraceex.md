---
description: Recupera le dimensioni e la posizione dell'elenco di moduli scaricati dinamicamente per il processo corrente.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330957"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="1aef4-103">RtlGetUnloadEventTraceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="1aef4-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="1aef4-104">Recupera le dimensioni e la posizione dell'elenco di moduli scaricati dinamicamente per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="1aef4-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aef4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1aef4-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="1aef4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1aef4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aef4-107">*ElementSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1aef4-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aef4-108">Puntatore a una variabile che contiene la dimensione di un elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="1aef4-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="1aef4-109">*Valore elementCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1aef4-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aef4-110">Puntatore a una variabile che contiene il numero di elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="1aef4-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="1aef4-111">*EventTrace* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1aef4-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aef4-112">Puntatore a una matrice di strutture **di \_ \_ \_ traccia degli eventi di scaricamento RTL** .</span><span class="sxs-lookup"><span data-stu-id="1aef4-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="1aef4-113">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1aef4-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aef4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1aef4-114">Return value</span></span>

<span data-ttu-id="1aef4-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1aef4-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aef4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1aef4-116">Remarks</span></span>

<span data-ttu-id="1aef4-117">Il caricatore archivia le informazioni sugli eventi scaricati in posizioni che possono essere lette nei processi sfruttando il fatto che Ntdll.dll viene caricato allo stesso indirizzo di base in tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="1aef4-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="1aef4-118">Quando un debugger deve eseguire una query sulle informazioni sui moduli scaricate, chiama questa funzione per determinare l'indirizzo in cui risiedono le variabili, quindi esegue una query sulla memoria virtuale nel processo di destinazione in corrispondenza di tali indirizzi per leggere i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="1aef4-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="1aef4-119">Ogni elemento nell'elenco è definito nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="1aef4-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="1aef4-120">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="1aef4-120">This function has no associated header file.</span></span> <span data-ttu-id="1aef4-121">La libreria di importazione associata, Ntdll. lib, è disponibile in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="1aef4-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="1aef4-122">È inoltre possibile chiamare questa funzione utilizzando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1aef4-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aef4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1aef4-123">Requirements</span></span>



| <span data-ttu-id="1aef4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aef4-124">Requirement</span></span> | <span data-ttu-id="1aef4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1aef4-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1aef4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1aef4-126">DLL</span></span><br/> | <dl> <span data-ttu-id="1aef4-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aef4-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
