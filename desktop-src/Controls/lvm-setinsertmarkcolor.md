---
title: Messaggio LVM_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore del punto di inserimento.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Controlli di Windows Message LVM_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963761"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="6cf9f-104">\_Messaggio SETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="6cf9f-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="6cf9f-105">Imposta il colore del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cf9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cf9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cf9f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6cf9f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6cf9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cf9f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6cf9f-110">Struttura **COLORREF** che specifica il colore per impostare il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf9f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cf9f-111">Return value</span></span>

<span data-ttu-id="6cf9f-112">Restituisce la struttura **COLORREF** impostata sul colore precedente.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cf9f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cf9f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6cf9f-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6cf9f-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6cf9f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6cf9f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cf9f-116">Requirements</span></span>



| <span data-ttu-id="6cf9f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf9f-117">Requirement</span></span> | <span data-ttu-id="6cf9f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6cf9f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf9f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf9f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cf9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cf9f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf9f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cf9f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cf9f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cf9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf9f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf9f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





