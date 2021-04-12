---
title: Messaggio LVM_GETEMPTYTEXT (COMmctrl. h)
description: Ottiene il testo destinato a essere visualizzato quando il controllo elenco-visualizzazione appare vuoto. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetEmptyText di ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Controlli di Windows Message LVM_GETEMPTYTEXT
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475167"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="d42df-105">\_Messaggio GETEMPTYTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="d42df-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="d42df-106">Ottiene il testo destinato a essere visualizzato quando il controllo elenco-visualizzazione appare vuoto.</span><span class="sxs-lookup"><span data-stu-id="d42df-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="d42df-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetEmptyText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .</span><span class="sxs-lookup"><span data-stu-id="d42df-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d42df-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d42df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d42df-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d42df-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d42df-110">Dimensioni del buffer a cui punta *lParam*, inclusa la terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="d42df-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d42df-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d42df-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d42df-112">Puntatore a un buffer Unicode con terminazione null di dimensioni specificate da *wParam* per ricevere il testo.</span><span class="sxs-lookup"><span data-stu-id="d42df-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="d42df-113">Il chiamante è responsabile dell'allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="d42df-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d42df-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d42df-114">Return value</span></span>

<span data-ttu-id="d42df-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d42df-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d42df-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d42df-116">Requirements</span></span>



| <span data-ttu-id="d42df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d42df-117">Requirement</span></span> | <span data-ttu-id="d42df-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d42df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d42df-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d42df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d42df-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d42df-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d42df-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d42df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d42df-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d42df-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d42df-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d42df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d42df-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d42df-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





