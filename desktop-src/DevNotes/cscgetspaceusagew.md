---
description: Recupera le informazioni sullo spazio utilizzato dalla cache File offline.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331197"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="2bc69-103">CSCGetSpaceUsageW (funzione)</span><span class="sxs-lookup"><span data-stu-id="2bc69-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="2bc69-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="2bc69-105">Recupera le informazioni sullo spazio utilizzato dalla cache File offline.</span><span class="sxs-lookup"><span data-stu-id="2bc69-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc69-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bc69-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="2bc69-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2bc69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc69-108">*lptzLocation* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-109">Percorso della directory della cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-110">*dwSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-111">Dimensioni del buffer *lptzLocation* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="2bc69-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-112">*lpdwMaxSpaceHigh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-113">**Valore DWORD** di ordine superiore del numero massimo di byte disponibili nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-114">*lpdwMaxSpaceLow* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-115">**Valore DWORD** di ordine inferiore del numero massimo di byte disponibili nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-116">*lpdwCurrentSpaceHigh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-117">**Valore DWORD** di ordine superiore del numero corrente di byte disponibili nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-118">*lpdwCurrentSpaceLow* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-119">**Valore DWORD** di ordine inferiore del numero corrente di byte disponibili nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-120">*lpcntTotalFiles* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-121">Numero totale di file nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="2bc69-122">*lpcntTotalDirs* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2bc69-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc69-123">Numero totale di directory nella cache.</span><span class="sxs-lookup"><span data-stu-id="2bc69-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc69-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bc69-124">Return value</span></span>

<span data-ttu-id="2bc69-125">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2bc69-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc69-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bc69-126">Remarks</span></span>

<span data-ttu-id="2bc69-127">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2bc69-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc69-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bc69-128">Requirements</span></span>



| <span data-ttu-id="2bc69-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc69-129">Requirement</span></span> | <span data-ttu-id="2bc69-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2bc69-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc69-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2bc69-131">DLL</span></span><br/> | <dl> <span data-ttu-id="2bc69-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bc69-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
