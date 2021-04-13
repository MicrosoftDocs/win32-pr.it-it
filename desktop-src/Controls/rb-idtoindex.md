---
title: Messaggio RB_IDTOINDEX (COMmctrl. h)
description: Converte un identificatore di banda in un indice di banda in un controllo Rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- Controlli di Windows Message RB_IDTOINDEX
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475346"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="0ad68-104">\_Messaggio IDTOINDEX RB</span><span class="sxs-lookup"><span data-stu-id="0ad68-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="0ad68-105">Converte un identificatore di banda in un indice di banda in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="0ad68-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ad68-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ad68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ad68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad68-108">Identificatore definito dall'applicazione della banda in questione.</span><span class="sxs-lookup"><span data-stu-id="0ad68-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="0ad68-109">Si tratta del valore passato nel membro **wid** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) quando è stata inserita la banda.</span><span class="sxs-lookup"><span data-stu-id="0ad68-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="0ad68-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ad68-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0ad68-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0ad68-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad68-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ad68-112">Return value</span></span>

<span data-ttu-id="0ad68-113">Restituisce l'indice della banda in base zero, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0ad68-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="0ad68-114">Se sono presenti identificatori di banda duplicati, viene restituito il primo.</span><span class="sxs-lookup"><span data-stu-id="0ad68-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad68-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ad68-115">Requirements</span></span>



| <span data-ttu-id="0ad68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad68-116">Requirement</span></span> | <span data-ttu-id="0ad68-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0ad68-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad68-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ad68-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad68-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ad68-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ad68-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ad68-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad68-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ad68-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ad68-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ad68-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ad68-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad68-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





