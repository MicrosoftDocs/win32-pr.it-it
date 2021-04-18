---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318429"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="ad93f-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="ad93f-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="ad93f-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="ad93f-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="ad93f-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad93f-105">Remarks</span></span>

<span data-ttu-id="ad93f-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ad93f-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ad93f-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ad93f-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ad93f-108">Se [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="ad93f-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad93f-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad93f-109">Requirements</span></span>



| <span data-ttu-id="ad93f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad93f-110">Requirement</span></span> | <span data-ttu-id="ad93f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ad93f-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad93f-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad93f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ad93f-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad93f-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad93f-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad93f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ad93f-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad93f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad93f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad93f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad93f-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad93f-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ad93f-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad93f-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad93f-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad93f-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ad93f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad93f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad93f-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="ad93f-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




