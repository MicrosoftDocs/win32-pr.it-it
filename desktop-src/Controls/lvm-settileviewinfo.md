---
title: Messaggio LVM_SETTILEVIEWINFO (COMmctrl. h)
description: Imposta le informazioni utilizzate da un controllo di visualizzazione elenco in visualizzazione affiancata.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- Controlli di Windows Message LVM_SETTILEVIEWINFO
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119458"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="10791-104">\_Messaggio SETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="10791-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="10791-105">Imposta le informazioni utilizzate da un controllo di visualizzazione elenco in visualizzazione affiancata.</span><span class="sxs-lookup"><span data-stu-id="10791-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="10791-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10791-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10791-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10791-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="10791-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10791-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10791-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10791-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> che contiene le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="10791-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10791-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10791-111">Return value</span></span>

<span data-ttu-id="10791-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="10791-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="10791-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="10791-113">Remarks</span></span>

<span data-ttu-id="10791-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="10791-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="10791-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10791-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10791-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10791-116">Requirements</span></span>



| <span data-ttu-id="10791-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10791-117">Requirement</span></span> | <span data-ttu-id="10791-118">Valore</span><span class="sxs-lookup"><span data-stu-id="10791-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10791-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10791-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10791-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10791-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10791-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10791-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10791-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10791-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10791-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10791-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10791-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10791-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





