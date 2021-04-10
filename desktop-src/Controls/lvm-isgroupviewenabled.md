---
title: Messaggio LVM_ISGROUPVIEWENABLED (COMmctrl. h)
description: Verifica se per il controllo di visualizzazione elenco è abilitata la visualizzazione gruppo.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- Controlli di Windows Message LVM_ISGROUPVIEWENABLED
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964732"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="1932d-104">\_Messaggio ISGROUPVIEWENABLED LVM</span><span class="sxs-lookup"><span data-stu-id="1932d-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="1932d-105">Verifica se per il controllo di visualizzazione elenco è abilitata la visualizzazione gruppo.</span><span class="sxs-lookup"><span data-stu-id="1932d-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="1932d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1932d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1932d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1932d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1932d-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1932d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1932d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1932d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1932d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1932d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1932d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1932d-111">Return value</span></span>

<span data-ttu-id="1932d-112">Restituisce **true** se la visualizzazione gruppo è abilitata o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1932d-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1932d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1932d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1932d-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1932d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1932d-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1932d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1932d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1932d-116">Requirements</span></span>



| <span data-ttu-id="1932d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1932d-117">Requirement</span></span> | <span data-ttu-id="1932d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1932d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1932d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1932d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1932d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1932d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1932d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1932d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1932d-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1932d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1932d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1932d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1932d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1932d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





