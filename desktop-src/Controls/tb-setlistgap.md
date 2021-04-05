---
title: Messaggio TB_SETLISTGAP (COMmctrl. h)
description: Imposta la distanza tra i pulsanti della barra degli strumenti su una barra degli strumenti specifica.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Controlli di Windows Message TB_SETLISTGAP
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873281"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="798d4-104">TB \_ SETLISTGAP messaggio</span><span class="sxs-lookup"><span data-stu-id="798d4-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="798d4-105">Imposta la distanza tra i pulsanti della barra degli strumenti su una barra degli strumenti specifica.</span><span class="sxs-lookup"><span data-stu-id="798d4-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="798d4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="798d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="798d4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="798d4-108">Gap, in pixel, tra i pulsanti sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="798d4-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="798d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="798d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="798d4-110">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="798d4-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798d4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="798d4-111">Return value</span></span>

<span data-ttu-id="798d4-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="798d4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="798d4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="798d4-113">Remarks</span></span>

<span data-ttu-id="798d4-114">Il gap tra i pulsanti si applica solo alla finestra di controllo della barra degli strumenti che riceve questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="798d4-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="798d4-115">La ricezione di questo messaggio attiva un ridisegno della barra degli strumenti, se la barra degli strumenti è attualmente visibile.</span><span class="sxs-lookup"><span data-stu-id="798d4-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="798d4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="798d4-116">Requirements</span></span>



| <span data-ttu-id="798d4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="798d4-117">Requirement</span></span> | <span data-ttu-id="798d4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="798d4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="798d4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="798d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="798d4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="798d4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="798d4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="798d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="798d4-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="798d4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="798d4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="798d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="798d4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="798d4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





