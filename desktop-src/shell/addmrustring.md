---
description: Aggiunge una stringa all'inizio dell'elenco MRU (Most Recently Used).
title: Funzione AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841192"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="3b4d0-103">Funzione AddMRUStringW</span><span class="sxs-lookup"><span data-stu-id="3b4d0-103">AddMRUStringW function</span></span>

<span data-ttu-id="3b4d0-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="3b4d0-105">Potrebbe essere stato modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="3b4d0-106">\]</span><span class="sxs-lookup"><span data-stu-id="3b4d0-106">\]</span></span>

<span data-ttu-id="3b4d0-107">Aggiunge una stringa all'inizio dell'elenco degli elementi usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4d0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b4d0-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="3b4d0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b4d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b4d0-110">*hMRU* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3b4d0-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4d0-111">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="3b4d0-111">Type: **HANDLE**</span></span>

<span data-ttu-id="3b4d0-112">Handle dell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="3b4d0-113">*szString* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3b4d0-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4d0-114">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="3b4d0-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="3b4d0-115">Puntatore ai dati.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-115">A pointer to the data.</span></span> <span data-ttu-id="3b4d0-116">Può trattarsi di una stringa o, se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** dati binari.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="3b4d0-117">Nel caso di dati binari, il primo **valore DWORD** ne indica le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b4d0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b4d0-118">Return value</span></span>

<span data-ttu-id="3b4d0-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3b4d0-119">Type: **int**</span></span>

<span data-ttu-id="3b4d0-120">Restituisce un valore non negativo in caso di esito positivo, -1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b4d0-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b4d0-121">Remarks</span></span>

<span data-ttu-id="3b4d0-122">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="3b4d0-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="3b4d0-123">È possibile accedervi tramite [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 401 per **AddMRUStringW.**</span><span class="sxs-lookup"><span data-stu-id="3b4d0-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b4d0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b4d0-124">Requirements</span></span>



| <span data-ttu-id="3b4d0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b4d0-125">Requirement</span></span> | <span data-ttu-id="3b4d0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3b4d0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4d0-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b4d0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3b4d0-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b4d0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b4d0-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b4d0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3b4d0-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b4d0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b4d0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3b4d0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b4d0-132"><dt>Comctl32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3b4d0-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3b4d0-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3b4d0-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3b4d0-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="3b4d0-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

