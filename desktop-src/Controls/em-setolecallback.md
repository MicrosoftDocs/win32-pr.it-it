---
title: Messaggio di EM_SETOLECALLBACK (RichEdit. h)
description: Fornisce un controllo Rich Edit di un oggetto IRichEditOleCallback che il controllo utilizza per ottenere le informazioni e le risorse correlate a OLE dal client.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Controlli di Windows Message EM_SETOLECALLBACK
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964389"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="bf5fe-104">\_Messaggio SETOLECALLBACK em</span><span class="sxs-lookup"><span data-stu-id="bf5fe-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="bf5fe-105">Fornisce un controllo Rich Edit di un oggetto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) che il controllo utilizza per ottenere le informazioni e le risorse correlate a OLE dal client.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf5fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf5fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf5fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf5fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5fe-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf5fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf5fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5fe-110">Puntatore a un oggetto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .</span><span class="sxs-lookup"><span data-stu-id="bf5fe-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="bf5fe-111">Il controllo chiama il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per l'oggetto prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf5fe-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf5fe-112">Return value</span></span>

<span data-ttu-id="bf5fe-113">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bf5fe-114">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5fe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf5fe-115">Requirements</span></span>



| <span data-ttu-id="bf5fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf5fe-116">Requirement</span></span> | <span data-ttu-id="bf5fe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bf5fe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5fe-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf5fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf5fe-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf5fe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf5fe-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf5fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf5fe-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf5fe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf5fe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf5fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf5fe-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fe-123"><dt>Richedit.h</dt></span></span> </dl> |



 

