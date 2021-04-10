---
description: Recupera un handle di oggetto per l'oggetto specificato associato al processo specificato.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Funzione ObFindHandleForObject (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877433"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="ad034-103">ObFindHandleForObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad034-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="ad034-104">\[Questa funzione è obsoleta e può essere modificata o non disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="ad034-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="ad034-105">Evitare di usare questa funzione.\]</span><span class="sxs-lookup"><span data-stu-id="ad034-105">Avoid using this function.\]</span></span>

<span data-ttu-id="ad034-106">Recupera un handle di oggetto per l'oggetto specificato associato al processo specificato.</span><span class="sxs-lookup"><span data-stu-id="ad034-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad034-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad034-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="ad034-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad034-109">*Processo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ad034-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad034-110">Processo.</span><span class="sxs-lookup"><span data-stu-id="ad034-110">The process.</span></span> <span data-ttu-id="ad034-111">Questo handle viene restituito dalla funzione **IoGetCurrentProcess** o **PsGetCurrentProcess** .</span><span class="sxs-lookup"><span data-stu-id="ad034-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="ad034-112">*Oggetto* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ad034-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad034-113">Puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad034-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="ad034-114">*Reserved1* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ad034-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad034-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ad034-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad034-116">*Reserved2* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ad034-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad034-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ad034-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad034-118">*Gestisci* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad034-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad034-119">Handle dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad034-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad034-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad034-120">Return value</span></span>

<span data-ttu-id="ad034-121">La funzione restituisce **true** se viene trovata una corrispondenza e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ad034-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad034-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad034-122">Remarks</span></span>

<span data-ttu-id="ad034-123">Questa funzione è disponibile in Ntoskrnl.exe e può essere chiamata solo dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="ad034-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="ad034-124">La libreria di importazione corrispondente è disponibile tramite Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="ad034-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad034-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad034-125">Requirements</span></span>



| <span data-ttu-id="ad034-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad034-126">Requirement</span></span> | <span data-ttu-id="ad034-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ad034-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad034-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad034-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad034-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad034-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ad034-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad034-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad034-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad034-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad034-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad034-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad034-133"><dt>Ntosp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad034-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="ad034-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad034-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad034-135"><dt>Ntoskrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad034-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




