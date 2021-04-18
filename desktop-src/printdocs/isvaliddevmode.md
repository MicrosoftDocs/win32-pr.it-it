---
description: La funzione IsValidDevmode verifica che il contenuto di una struttura DEVMODE sia valido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Funzione IsValidDevmode (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318372"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="598e6-103">IsValidDevmode (funzione)</span><span class="sxs-lookup"><span data-stu-id="598e6-103">IsValidDevmode function</span></span>

<span data-ttu-id="598e6-104">La funzione **IsValidDevmode** verifica che il contenuto di una struttura DEVMODE sia valido.</span><span class="sxs-lookup"><span data-stu-id="598e6-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="598e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="598e6-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="598e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="598e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598e6-107">*pDevmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="598e6-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598e6-108">Puntatore alla [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da convalidare.</span><span class="sxs-lookup"><span data-stu-id="598e6-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="598e6-109">*DevmodeSize*</span><span class="sxs-lookup"><span data-stu-id="598e6-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="598e6-110">Dimensioni in byte del buffer di byte di input.</span><span class="sxs-lookup"><span data-stu-id="598e6-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598e6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="598e6-111">Return value</span></span>

<span data-ttu-id="598e6-112">**True** se l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) è strutturalmente valido.</span><span class="sxs-lookup"><span data-stu-id="598e6-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="598e6-113">Se vengono rilevati errori secondari, la funzione li correggerà e restituirà **true**.</span><span class="sxs-lookup"><span data-stu-id="598e6-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="598e6-114">**False** se [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) presenta uno o più problemi strutturali significativi.</span><span class="sxs-lookup"><span data-stu-id="598e6-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="598e6-115">Il membro **dmSize** , ad esempio, non è allineato correttamente o specifica un buffer troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="598e6-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="598e6-116">**False** anche se **pDevmode** è **null**.</span><span class="sxs-lookup"><span data-stu-id="598e6-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="598e6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="598e6-117">Remarks</span></span>

<span data-ttu-id="598e6-118">Non sono controllati campi di driver della stampante privati di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , ma solo i campi pubblici.</span><span class="sxs-lookup"><span data-stu-id="598e6-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="598e6-119">I chiamanti devono usare **dmSize** + **dmDriverExtra** per **DevmodeSize** solo se possono garantire che la dimensione del buffer di input sia almeno quella grande.</span><span class="sxs-lookup"><span data-stu-id="598e6-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="598e6-120">Poiché [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) è generalmente dati non attendibili, anche i valori presenti nel buffer di input in corrispondenza degli offset **dmSize** e **dmDriverExtra** non sono attendibili.</span><span class="sxs-lookup"><span data-stu-id="598e6-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="598e6-121">Questa funzione è eseguibile nel contesto di Least-Privileged account utente (LUA).</span><span class="sxs-lookup"><span data-stu-id="598e6-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="598e6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="598e6-122">Requirements</span></span>



| <span data-ttu-id="598e6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="598e6-123">Requirement</span></span> | <span data-ttu-id="598e6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="598e6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="598e6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="598e6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="598e6-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="598e6-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="598e6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="598e6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="598e6-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="598e6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="598e6-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="598e6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="598e6-130"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="598e6-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="598e6-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="598e6-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="598e6-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="598e6-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="598e6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="598e6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598e6-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="598e6-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="598e6-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="598e6-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="598e6-136">**IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="598e6-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="598e6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="598e6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598e6-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="598e6-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="598e6-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="598e6-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="598e6-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="598e6-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




