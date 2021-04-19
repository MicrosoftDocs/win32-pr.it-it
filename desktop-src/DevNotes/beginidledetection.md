---
description: Inizia il monitoraggio dell'inattività.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329890"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="363f8-103">BeginIdleDetection (funzione)</span><span class="sxs-lookup"><span data-stu-id="363f8-103">BeginIdleDetection function</span></span>

<span data-ttu-id="363f8-104">\[Questa funzione non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="363f8-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="363f8-105">Usare invece la funzione **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="363f8-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="363f8-106">Inizia il monitoraggio dell'inattività.</span><span class="sxs-lookup"><span data-stu-id="363f8-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="363f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="363f8-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="363f8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="363f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363f8-109">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="363f8-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="363f8-110">Funzione chiamata quando lo stato di inattività viene modificato.</span><span class="sxs-lookup"><span data-stu-id="363f8-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="363f8-111">Questo callback viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="363f8-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="363f8-112">*dwIdleMin*</span><span class="sxs-lookup"><span data-stu-id="363f8-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="363f8-113">Numero di minuti di inattività prima che venga effettuata la chiamata alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="363f8-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="363f8-114">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="363f8-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="363f8-115">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="363f8-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363f8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="363f8-116">Return value</span></span>

<span data-ttu-id="363f8-117">Restituisce 0 se la funzione ha esito positivo; in caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="363f8-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="363f8-118">Se, ad esempio, il valore di *dwReserved* è diverso da 0, vengono restituiti **\_ \_ dati non validi** .</span><span class="sxs-lookup"><span data-stu-id="363f8-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="363f8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="363f8-119">Remarks</span></span>

<span data-ttu-id="363f8-120">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="363f8-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="363f8-121">Questa funzione non viene esportata per nome; specificare il numero ordinale 3 quando si chiama **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="363f8-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="363f8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="363f8-122">Requirements</span></span>



| <span data-ttu-id="363f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="363f8-123">Requirement</span></span> | <span data-ttu-id="363f8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="363f8-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="363f8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="363f8-125">DLL</span></span><br/> | <dl> <span data-ttu-id="363f8-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363f8-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363f8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="363f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363f8-128">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="363f8-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
