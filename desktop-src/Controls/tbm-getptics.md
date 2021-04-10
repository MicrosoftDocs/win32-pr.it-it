---
title: Messaggio TBM_GETPTICS (COMmctrl. h)
description: Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Controlli di Windows Message TBM_GETPTICS
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964253"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="a37e9-104">\_Messaggio GETPTICS TBM</span><span class="sxs-lookup"><span data-stu-id="a37e9-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="a37e9-105">Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a37e9-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a37e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a37e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a37e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a37e9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a37e9-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a37e9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a37e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a37e9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a37e9-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a37e9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a37e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a37e9-111">Return value</span></span>

<span data-ttu-id="a37e9-112">Restituisce l'indirizzo di una matrice di valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a37e9-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="a37e9-113">Gli elementi della matrice specificano le posizioni logiche dei segni di graduazione del TrackBar, escluso il primo e l'ultimo segno di graduazione creato dal TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a37e9-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="a37e9-114">Le posizioni logiche possono essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a37e9-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="a37e9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a37e9-115">Remarks</span></span>

<span data-ttu-id="a37e9-116">Il numero di elementi nella matrice è inferiore a due rispetto al conteggio restituito dal messaggio [**\_ GETNUMTICS TBM**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="a37e9-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="a37e9-117">Si noti che i valori nella matrice possono includere posizioni duplicate e che potrebbero non essere in ordine sequenziale.</span><span class="sxs-lookup"><span data-stu-id="a37e9-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="a37e9-118">Il puntatore restituito è valido fino a quando non si modificano i segni di graduazione del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a37e9-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a37e9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37e9-119">Requirements</span></span>



| <span data-ttu-id="a37e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a37e9-120">Requirement</span></span> | <span data-ttu-id="a37e9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a37e9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a37e9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a37e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a37e9-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a37e9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a37e9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a37e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a37e9-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a37e9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a37e9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a37e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a37e9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a37e9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





