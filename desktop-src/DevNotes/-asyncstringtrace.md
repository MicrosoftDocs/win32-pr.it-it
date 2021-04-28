---
description: 'Funzione AsyncStringTrace: completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile sprintf.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Funzione AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085799"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="a24e3-103">Funzione AsyncStringTrace</span><span class="sxs-lookup"><span data-stu-id="a24e3-103">AsyncStringTrace function</span></span>

<span data-ttu-id="a24e3-104">Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile **sprintf.**</span><span class="sxs-lookup"><span data-stu-id="a24e3-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="a24e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a24e3-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="a24e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a24e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24e3-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a24e3-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24e3-108">Parametro di traccia a 32 bit utilizzato per il filtro a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="a24e3-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="a24e3-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="a24e3-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a24e3-110">Stringa con terminazione zero che descrive il formato della traccia.</span><span class="sxs-lookup"><span data-stu-id="a24e3-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="a24e3-111">*Marcatore*</span><span class="sxs-lookup"><span data-stu-id="a24e3-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="a24e3-112">Marcatore per **le funzioni vsprintf.**</span><span class="sxs-lookup"><span data-stu-id="a24e3-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24e3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a24e3-113">Return value</span></span>

<span data-ttu-id="a24e3-114">Questa funzione restituisce la lunghezza dell'istruzione di traccia, in byte.</span><span class="sxs-lookup"><span data-stu-id="a24e3-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24e3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a24e3-115">Remarks</span></span>

<span data-ttu-id="a24e3-116">Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="a24e3-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="a24e3-117">Il **tipo di dati va \_ list** è un tipo standard usato per contenere le informazioni necessarie per le macro **va \_ arg** e **va \_ end.**</span><span class="sxs-lookup"><span data-stu-id="a24e3-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="a24e3-118">Per altre informazioni, vedere [Tipi standard.](/cpp/c-runtime-library/standard-types?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="a24e3-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="a24e3-119">A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="a24e3-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24e3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a24e3-120">Requirements</span></span>



| <span data-ttu-id="a24e3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a24e3-121">Requirement</span></span> | <span data-ttu-id="a24e3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a24e3-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a24e3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a24e3-123">DLL</span></span><br/> | <dl> <span data-ttu-id="a24e3-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a24e3-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

