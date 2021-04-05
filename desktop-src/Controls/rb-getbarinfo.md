---
title: Messaggio RB_GETBARINFO (COMmctrl. h)
description: Recupera le informazioni sul controllo Rebar e sull'elenco di immagini utilizzate.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Controlli di Windows Message RB_GETBARINFO
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048549"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="34529-104">\_Messaggio GETBARINFO RB</span><span class="sxs-lookup"><span data-stu-id="34529-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="34529-105">Recupera le informazioni sul controllo Rebar e sull'elenco di immagini utilizzate.</span><span class="sxs-lookup"><span data-stu-id="34529-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="34529-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34529-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34529-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="34529-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="34529-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="34529-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34529-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34529-110">Puntatore a una struttura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) che riceverà le informazioni sul controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="34529-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="34529-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(REBARINFO).</span><span class="sxs-lookup"><span data-stu-id="34529-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34529-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34529-112">Return value</span></span>

<span data-ttu-id="34529-113">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="34529-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="34529-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34529-114">Requirements</span></span>



| <span data-ttu-id="34529-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34529-115">Requirement</span></span> | <span data-ttu-id="34529-116">Valore</span><span class="sxs-lookup"><span data-stu-id="34529-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34529-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34529-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34529-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34529-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34529-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34529-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34529-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34529-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34529-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34529-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="34529-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34529-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





