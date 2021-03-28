---
description: Aggiunge una stringa all'inizio dell'elenco degli ultimi elementi usati (MRU).
title: AddMRUStringW (funzione)
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049374"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="60ded-103">AddMRUStringW (funzione)</span><span class="sxs-lookup"><span data-stu-id="60ded-103">AddMRUStringW function</span></span>

<span data-ttu-id="60ded-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60ded-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="60ded-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="60ded-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="60ded-106">\]</span><span class="sxs-lookup"><span data-stu-id="60ded-106">\]</span></span>

<span data-ttu-id="60ded-107">Aggiunge una stringa all'inizio dell'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="60ded-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ded-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60ded-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="60ded-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60ded-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ded-110">*hMRU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60ded-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ded-111">Tipo: **handle**</span><span class="sxs-lookup"><span data-stu-id="60ded-111">Type: **HANDLE**</span></span>

<span data-ttu-id="60ded-112">Handle dell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="60ded-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="60ded-113">*szString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60ded-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ded-114">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="60ded-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="60ded-115">Puntatore ai dati.</span><span class="sxs-lookup"><span data-stu-id="60ded-115">A pointer to the data.</span></span> <span data-ttu-id="60ded-116">Può essere una stringa o, se l'elenco MRU è stato creato con il flag **\_ binario MRU** , dati binari.</span><span class="sxs-lookup"><span data-stu-id="60ded-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="60ded-117">Nel caso dei dati binari, il primo **valore DWORD** ne indica le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="60ded-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ded-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60ded-118">Return value</span></span>

<span data-ttu-id="60ded-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="60ded-119">Type: **int**</span></span>

<span data-ttu-id="60ded-120">Restituisce un valore non negativo se ha esito positivo,-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="60ded-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ded-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="60ded-121">Remarks</span></span>

<span data-ttu-id="60ded-122">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="60ded-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="60ded-123">È possibile accedervi tramite [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o estratti da comctl32.dll in base al relativo ordinale, ovvero 401 per **AddMRUStringW**.</span><span class="sxs-lookup"><span data-stu-id="60ded-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ded-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60ded-124">Requirements</span></span>



| <span data-ttu-id="60ded-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ded-125">Requirement</span></span> | <span data-ttu-id="60ded-126">Valore</span><span class="sxs-lookup"><span data-stu-id="60ded-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ded-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60ded-127">Minimum supported client</span></span><br/> | <span data-ttu-id="60ded-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60ded-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60ded-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60ded-129">Minimum supported server</span></span><br/> | <span data-ttu-id="60ded-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60ded-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60ded-131">DLL</span><span class="sxs-lookup"><span data-stu-id="60ded-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60ded-132"><dt>Comctl32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="60ded-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="60ded-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="60ded-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="60ded-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="60ded-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

