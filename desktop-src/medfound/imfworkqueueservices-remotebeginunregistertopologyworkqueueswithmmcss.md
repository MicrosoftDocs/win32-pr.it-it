---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: BeginUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882834"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="fd2ff-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="fd2ff-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="fd2ff-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="fd2ff-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="fd2ff-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd2ff-105">Remarks</span></span>

<span data-ttu-id="fd2ff-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fd2ff-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="fd2ff-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd2ff-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="fd2ff-108">Se [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="fd2ff-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2ff-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd2ff-109">Requirements</span></span>



| <span data-ttu-id="fd2ff-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2ff-110">Requirement</span></span> | <span data-ttu-id="fd2ff-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fd2ff-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2ff-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd2ff-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2ff-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd2ff-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fd2ff-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd2ff-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2ff-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd2ff-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd2ff-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd2ff-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd2ff-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd2ff-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd2ff-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd2ff-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd2ff-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd2ff-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="fd2ff-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd2ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2ff-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="fd2ff-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




