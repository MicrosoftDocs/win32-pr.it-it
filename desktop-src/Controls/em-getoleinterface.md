---
title: Messaggio di EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera un oggetto IRichEditOle che può essere utilizzato da un client per accedere a una funzionalità di Component Object Model (COM) del controllo Rich Edit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Controlli di Windows Message EM_GETOLEINTERFACE
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120530"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="f24c6-104">\_Messaggio GETOLEINTERFACE em</span><span class="sxs-lookup"><span data-stu-id="f24c6-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="f24c6-105">Recupera un oggetto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) che può essere utilizzato da un client per accedere a una funzionalità di Component Object Model (com) del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f24c6-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="f24c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f24c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f24c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f24c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f24c6-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f24c6-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f24c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f24c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f24c6-110">Puntatore a un puntatore che riceve l'oggetto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="f24c6-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="f24c6-111">Il controllo chiama il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per l'oggetto prima della restituzione, quindi l'applicazione chiamante deve chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando viene eseguita con l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f24c6-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f24c6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f24c6-112">Return value</span></span>

<span data-ttu-id="f24c6-113">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f24c6-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f24c6-114">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="f24c6-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f24c6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f24c6-115">Requirements</span></span>



| <span data-ttu-id="f24c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f24c6-116">Requirement</span></span> | <span data-ttu-id="f24c6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f24c6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f24c6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f24c6-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f24c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f24c6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f24c6-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f24c6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f24c6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f24c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f24c6-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24c6-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24c6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f24c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24c6-125">**IRichEditOle**</span><span class="sxs-lookup"><span data-stu-id="f24c6-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

