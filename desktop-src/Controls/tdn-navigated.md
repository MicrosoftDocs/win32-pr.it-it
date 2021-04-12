---
title: Codice di notifica TDN_NAVIGATED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando si è verificata la navigazione. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- Controlli di Windows per il codice di notifica TDN_NAVIGATED
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519048"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="a91fc-105">TDN \_ codice di notifica navigato</span><span class="sxs-lookup"><span data-stu-id="a91fc-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="a91fc-106">Inviato da una finestra di dialogo attività quando si è verificata la navigazione.</span><span class="sxs-lookup"><span data-stu-id="a91fc-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="a91fc-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="a91fc-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a91fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a91fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a91fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a91fc-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a91fc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a91fc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a91fc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a91fc-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a91fc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91fc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a91fc-113">Return value</span></span>

<span data-ttu-id="a91fc-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a91fc-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91fc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a91fc-115">Requirements</span></span>



| <span data-ttu-id="a91fc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a91fc-116">Requirement</span></span> | <span data-ttu-id="a91fc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a91fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a91fc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a91fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a91fc-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a91fc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a91fc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a91fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a91fc-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a91fc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a91fc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a91fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a91fc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a91fc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





