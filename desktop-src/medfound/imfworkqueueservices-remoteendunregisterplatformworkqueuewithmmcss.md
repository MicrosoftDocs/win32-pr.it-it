---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884674"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="c6ff1-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="c6ff1-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="c6ff1-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="c6ff1-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="c6ff1-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6ff1-105">Remarks</span></span>

<span data-ttu-id="c6ff1-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c6ff1-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c6ff1-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c6ff1-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c6ff1-108">Se [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="c6ff1-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ff1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6ff1-109">Requirements</span></span>



| <span data-ttu-id="c6ff1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ff1-110">Requirement</span></span> | <span data-ttu-id="c6ff1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c6ff1-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ff1-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ff1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ff1-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6ff1-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6ff1-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ff1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ff1-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6ff1-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6ff1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6ff1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ff1-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6ff1-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c6ff1-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6ff1-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6ff1-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6ff1-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c6ff1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6ff1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ff1-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="c6ff1-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




