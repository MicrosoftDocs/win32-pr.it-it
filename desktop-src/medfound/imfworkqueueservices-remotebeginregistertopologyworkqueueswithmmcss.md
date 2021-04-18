---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: RemoteBeginRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317311"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="e93f8-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="e93f8-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="e93f8-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="e93f8-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="e93f8-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="e93f8-105">Remarks</span></span>

<span data-ttu-id="e93f8-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e93f8-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="e93f8-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e93f8-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="e93f8-108">Se [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="e93f8-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93f8-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e93f8-109">Requirements</span></span>



| <span data-ttu-id="e93f8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e93f8-110">Requirement</span></span> | <span data-ttu-id="e93f8-111">Valore</span><span class="sxs-lookup"><span data-stu-id="e93f8-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93f8-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e93f8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e93f8-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e93f8-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e93f8-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e93f8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e93f8-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e93f8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e93f8-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e93f8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e93f8-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e93f8-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="e93f8-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e93f8-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="e93f8-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e93f8-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e93f8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e93f8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93f8-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="e93f8-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




