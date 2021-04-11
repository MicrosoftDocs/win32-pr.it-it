---
title: Messaggio RB_GETROWHEIGHT (COMmctrl. h)
description: Recupera l'altezza di una riga specificata in un controllo Rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Controlli di Windows Message RB_GETROWHEIGHT
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874113"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="dc6ad-104">\_Messaggio GETROWHEIGHT RB</span><span class="sxs-lookup"><span data-stu-id="dc6ad-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="dc6ad-105">Recupera l'altezza di una riga specificata in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc6ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc6ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc6ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6ad-108">Indice in base zero di una banda.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-108">Zero-based index of a band.</span></span> <span data-ttu-id="dc6ad-109">Verrà recuperata l'altezza della riga che contiene la banda specificata.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dc6ad-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc6ad-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc6ad-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6ad-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc6ad-112">Return value</span></span>

<span data-ttu-id="dc6ad-113">Restituisce un valore **uint** che rappresenta l'altezza della riga, in pixel.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc6ad-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc6ad-114">Remarks</span></span>

<span data-ttu-id="dc6ad-115">Per recuperare il numero di righe in un controllo Rebar, utilizzare il messaggio [**RB \_ GetRowCount**](rb-getrowcount.md) .</span><span class="sxs-lookup"><span data-stu-id="dc6ad-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6ad-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc6ad-116">Requirements</span></span>



| <span data-ttu-id="dc6ad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc6ad-117">Requirement</span></span> | <span data-ttu-id="dc6ad-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ad-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ad-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc6ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6ad-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc6ad-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc6ad-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc6ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6ad-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc6ad-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc6ad-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc6ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc6ad-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc6ad-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





