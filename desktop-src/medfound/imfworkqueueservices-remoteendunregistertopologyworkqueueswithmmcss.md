---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314043"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="e3719-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="e3719-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="e3719-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="e3719-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="e3719-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3719-105">Remarks</span></span>

<span data-ttu-id="e3719-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e3719-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="e3719-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e3719-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="e3719-108">Se [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="e3719-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3719-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3719-109">Requirements</span></span>



| <span data-ttu-id="e3719-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3719-110">Requirement</span></span> | <span data-ttu-id="e3719-111">Valore</span><span class="sxs-lookup"><span data-stu-id="e3719-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3719-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3719-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e3719-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3719-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3719-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3719-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e3719-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3719-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3719-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3719-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3719-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3719-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="e3719-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3719-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3719-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3719-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e3719-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3719-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3719-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="e3719-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




