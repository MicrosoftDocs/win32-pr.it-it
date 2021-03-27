---
description: Consente di creare un nuovo elenco degli ultimi elementi usati (MRU).
title: CreateMRUListW (funzione)
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
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750247"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="d93dd-103">CreateMRUListW (funzione)</span><span class="sxs-lookup"><span data-stu-id="d93dd-103">CreateMRUListW function</span></span>

<span data-ttu-id="d93dd-104">Consente di creare un nuovo elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="d93dd-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d93dd-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="d93dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d93dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93dd-107">*lpmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d93dd-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93dd-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="d93dd-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="d93dd-109">Puntatore a una struttura [**MRUINFO**](mruinfo.md) che definisce l'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="d93dd-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93dd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d93dd-110">Return value</span></span>

<span data-ttu-id="d93dd-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d93dd-111">Type: **int**</span></span>

<span data-ttu-id="d93dd-112">Restituisce un handle per il nuovo elenco MRU oppure 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="d93dd-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d93dd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d93dd-113">Remarks</span></span>

<span data-ttu-id="d93dd-114">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="d93dd-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="d93dd-115">È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estratti da comctl32.dll in base al relativo ordinale, ovvero 400 per **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="d93dd-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93dd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d93dd-116">Requirements</span></span>



| <span data-ttu-id="d93dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d93dd-117">Requirement</span></span> | <span data-ttu-id="d93dd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d93dd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93dd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d93dd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d93dd-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d93dd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d93dd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d93dd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d93dd-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d93dd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d93dd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d93dd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d93dd-124"><dt>Comctl32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d93dd-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d93dd-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d93dd-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d93dd-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="d93dd-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
