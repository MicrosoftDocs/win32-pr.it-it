---
title: Messaggio TB_GETMETRICS (COMmctrl. h)
description: Recupera le metriche di un controllo della barra degli strumenti.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- Controlli di Windows Message TB_GETMETRICS
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874217"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="58f8c-104">\_Messaggio GETmetrics TB</span><span class="sxs-lookup"><span data-stu-id="58f8c-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="58f8c-105">Recupera le metriche di un controllo della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="58f8c-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="58f8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58f8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f8c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58f8c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="58f8c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="58f8c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="58f8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58f8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58f8c-110">Puntatore a una struttura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) che riceve le metriche della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="58f8c-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f8c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58f8c-111">Return value</span></span>

<span data-ttu-id="58f8c-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="58f8c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f8c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58f8c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58f8c-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="58f8c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="58f8c-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="58f8c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58f8c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58f8c-116">Requirements</span></span>



| <span data-ttu-id="58f8c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f8c-117">Requirement</span></span> | <span data-ttu-id="58f8c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="58f8c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58f8c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58f8c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58f8c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58f8c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58f8c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58f8c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58f8c-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58f8c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58f8c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58f8c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58f8c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58f8c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





