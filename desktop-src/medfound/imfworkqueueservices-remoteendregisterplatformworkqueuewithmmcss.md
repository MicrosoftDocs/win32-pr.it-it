---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749199"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="cdf79-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="cdf79-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="cdf79-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="cdf79-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="cdf79-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdf79-105">Remarks</span></span>

<span data-ttu-id="cdf79-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cdf79-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="cdf79-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cdf79-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="cdf79-108">Se [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="cdf79-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf79-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdf79-109">Requirements</span></span>



| <span data-ttu-id="cdf79-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf79-110">Requirement</span></span> | <span data-ttu-id="cdf79-111">Valore</span><span class="sxs-lookup"><span data-stu-id="cdf79-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf79-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf79-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf79-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdf79-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cdf79-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf79-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf79-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdf79-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cdf79-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdf79-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdf79-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdf79-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="cdf79-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdf79-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdf79-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdf79-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cdf79-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf79-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf79-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="cdf79-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




