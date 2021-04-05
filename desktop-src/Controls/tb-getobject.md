---
title: Messaggio TB_GETOBJECT (COMmctrl. h)
description: Recupera l'oggetto IDropTarget per un controllo Toolbar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Controlli di Windows Message TB_GETOBJECT
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120687"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="d04a9-104">TB- \_ messaggio GETobject</span><span class="sxs-lookup"><span data-stu-id="d04a9-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="d04a9-105">Recupera l'oggetto [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) per un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="d04a9-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d04a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d04a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d04a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d04a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d04a9-108">Identificatore dell'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="d04a9-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="d04a9-109">Questo valore deve puntare all' **IID \_ IDropTarget**.</span><span class="sxs-lookup"><span data-stu-id="d04a9-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="d04a9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d04a9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d04a9-111">Indirizzo che riceve il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d04a9-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="d04a9-112">Se si verifica un errore, in questo indirizzo viene inserito un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d04a9-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d04a9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d04a9-113">Return value</span></span>

<span data-ttu-id="d04a9-114">Restituisce un valore **HRESULT** che indica l'esito positivo o negativo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d04a9-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d04a9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d04a9-115">Remarks</span></span>

<span data-ttu-id="d04a9-116">Il [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) della barra degli strumenti viene usato dalla barra degli strumenti quando gli oggetti vengono trascinati su di esso.</span><span class="sxs-lookup"><span data-stu-id="d04a9-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04a9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d04a9-117">Requirements</span></span>



| <span data-ttu-id="d04a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d04a9-118">Requirement</span></span> | <span data-ttu-id="d04a9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d04a9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d04a9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d04a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d04a9-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d04a9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d04a9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d04a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d04a9-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d04a9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d04a9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d04a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d04a9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d04a9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

