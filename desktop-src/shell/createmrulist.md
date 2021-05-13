---
description: Crea un nuovo elenco degli elementi usati più di recente.
title: Funzione CreateMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843382"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="7bb9b-103">Funzione CreateMRUListW</span><span class="sxs-lookup"><span data-stu-id="7bb9b-103">CreateMRUListW function</span></span>

<span data-ttu-id="7bb9b-104">Crea un nuovo elenco degli elementi usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="7bb9b-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb9b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bb9b-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="7bb9b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bb9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb9b-107">*lpmi* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7bb9b-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9b-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="7bb9b-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="7bb9b-109">Puntatore a una [**struttura MRUINFO**](mruinfo.md) che definisce l'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="7bb9b-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb9b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bb9b-110">Return value</span></span>

<span data-ttu-id="7bb9b-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7bb9b-111">Type: **int**</span></span>

<span data-ttu-id="7bb9b-112">Restituisce un handle per il nuovo elenco MRU oppure 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="7bb9b-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb9b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bb9b-113">Remarks</span></span>

<span data-ttu-id="7bb9b-114">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="7bb9b-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="7bb9b-115">È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 400 per **CreateMRUListW.**</span><span class="sxs-lookup"><span data-stu-id="7bb9b-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb9b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bb9b-116">Requirements</span></span>



| <span data-ttu-id="7bb9b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb9b-117">Requirement</span></span> | <span data-ttu-id="7bb9b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7bb9b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb9b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bb9b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb9b-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bb9b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7bb9b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bb9b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb9b-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bb9b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7bb9b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb9b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb9b-124"><dt>Comctl32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb9b-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="7bb9b-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7bb9b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7bb9b-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="7bb9b-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
