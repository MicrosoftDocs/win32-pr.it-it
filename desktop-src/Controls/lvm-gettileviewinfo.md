---
title: Messaggio LVM_GETTILEVIEWINFO (COMmctrl. h)
description: Recupera le informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- Controlli di Windows Message LVM_GETTILEVIEWINFO
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742983"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="4930f-104">\_Messaggio GETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="4930f-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="4930f-105">Recupera le informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.</span><span class="sxs-lookup"><span data-stu-id="4930f-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="4930f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4930f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4930f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4930f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4930f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4930f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4930f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4930f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4930f-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> che riceve le informazioni recuperate.</span><span class="sxs-lookup"><span data-stu-id="4930f-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4930f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4930f-111">Return value</span></span>

<span data-ttu-id="4930f-112">Valore restituito non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4930f-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4930f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4930f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4930f-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="4930f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4930f-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4930f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4930f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4930f-116">Requirements</span></span>



| <span data-ttu-id="4930f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4930f-117">Requirement</span></span> | <span data-ttu-id="4930f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4930f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4930f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4930f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4930f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4930f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4930f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4930f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4930f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4930f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4930f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4930f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4930f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4930f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





