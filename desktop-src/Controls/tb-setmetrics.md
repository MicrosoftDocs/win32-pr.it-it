---
title: Messaggio TB_SETMETRICS (COMmctrl. h)
description: Imposta la metrica di un controllo della barra degli strumenti.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- Controlli di Windows Message TB_SETMETRICS
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963936"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="313b9-104">\_Messaggio SEmetrics TB</span><span class="sxs-lookup"><span data-stu-id="313b9-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="313b9-105">Imposta la metrica di un controllo della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="313b9-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="313b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="313b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="313b9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="313b9-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="313b9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="313b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="313b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313b9-110">Struttura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) che contiene le metriche della barra degli strumenti da impostare.</span><span class="sxs-lookup"><span data-stu-id="313b9-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313b9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="313b9-111">Return value</span></span>

<span data-ttu-id="313b9-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="313b9-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="313b9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="313b9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="313b9-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="313b9-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="313b9-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="313b9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="313b9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="313b9-116">Requirements</span></span>



| <span data-ttu-id="313b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="313b9-117">Requirement</span></span> | <span data-ttu-id="313b9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="313b9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313b9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="313b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="313b9-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="313b9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="313b9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="313b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="313b9-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="313b9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="313b9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="313b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="313b9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="313b9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





