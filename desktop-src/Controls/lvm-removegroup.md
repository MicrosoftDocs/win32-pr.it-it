---
title: Messaggio LVM_REMOVEGROUP (COMmctrl. h)
description: Rimuove un gruppo da un controllo visualizzazione elenco.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- Controlli di Windows Message LVM_REMOVEGROUP
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964473"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="0e97c-104">\_Messaggio REMOVEGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="0e97c-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="0e97c-105">Rimuove un gruppo da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0e97c-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e97c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e97c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e97c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e97c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e97c-108">ID che specifica il gruppo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0e97c-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="0e97c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e97c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e97c-110">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0e97c-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e97c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e97c-111">Return value</span></span>

<span data-ttu-id="0e97c-112">Restituisce l'indice del gruppo, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0e97c-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e97c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e97c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e97c-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="0e97c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0e97c-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0e97c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e97c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e97c-116">Requirements</span></span>



| <span data-ttu-id="0e97c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e97c-117">Requirement</span></span> | <span data-ttu-id="0e97c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0e97c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e97c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e97c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e97c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e97c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e97c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e97c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e97c-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e97c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e97c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e97c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e97c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e97c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





