---
title: TsViewCookie (Textstor. h)
description: Il tipo di dati TsViewCookie identifica una visualizzazione del contesto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301248"
---
# <a name="tsviewcookie"></a><span data-ttu-id="fc469-104">TsViewCookie</span><span class="sxs-lookup"><span data-stu-id="fc469-104">TsViewCookie</span></span>

<span data-ttu-id="fc469-105">Il tipo di dati **TsViewCookie** identifica una visualizzazione del contesto.</span><span class="sxs-lookup"><span data-stu-id="fc469-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="fc469-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc469-106">Remarks</span></span>

<span data-ttu-id="fc469-107">Un'applicazione deve fornire un valore **TsViewCookie** univoco per ogni vista creata.</span><span class="sxs-lookup"><span data-stu-id="fc469-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="fc469-108">Gestione TSF ottiene questo valore dall'applicazione chiamando [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) o [ITextStoreAnchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="fc469-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="fc469-109">Il gestore TSF utilizza questo valore per identificare la vista quando vengono chiamati diversi metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) o [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="fc469-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc469-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc469-110">Requirements</span></span>



| <span data-ttu-id="fc469-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc469-111">Requirement</span></span> | <span data-ttu-id="fc469-112">Valore</span><span class="sxs-lookup"><span data-stu-id="fc469-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc469-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc469-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc469-114">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="fc469-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="fc469-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc469-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc469-116">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fc469-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="fc469-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fc469-117">Redistributable</span></span><br/>          | <span data-ttu-id="fc469-118">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc469-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="fc469-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc469-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc469-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc469-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc469-121">IDL</span><span class="sxs-lookup"><span data-stu-id="fc469-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc469-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc469-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc469-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc469-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc469-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="fc469-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="fc469-125">**ITextStoreACP:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="fc469-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="fc469-126">**ITextStoreAnchor:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="fc469-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





