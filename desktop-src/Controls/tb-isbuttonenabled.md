---
title: Messaggio TB_ISBUTTONENABLED (COMmctrl. h)
description: Determina se il pulsante specificato in una barra degli strumenti è abilitato.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- Controlli di Windows Message TB_ISBUTTONENABLED
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873577"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="82c39-104">TB \_ ISBUTTONENABLED messaggio</span><span class="sxs-lookup"><span data-stu-id="82c39-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="82c39-105">Determina se il pulsante specificato in una barra degli strumenti è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82c39-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="82c39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82c39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c39-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82c39-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82c39-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="82c39-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="82c39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82c39-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82c39-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="82c39-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82c39-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82c39-111">Return value</span></span>

<span data-ttu-id="82c39-112">Restituisce un valore diverso da zero se il pulsante è abilitato oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82c39-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82c39-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82c39-113">Requirements</span></span>



| <span data-ttu-id="82c39-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82c39-114">Requirement</span></span> | <span data-ttu-id="82c39-115">Valore</span><span class="sxs-lookup"><span data-stu-id="82c39-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82c39-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82c39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82c39-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82c39-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82c39-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82c39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82c39-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82c39-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82c39-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82c39-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="82c39-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82c39-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





