---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: RemoteBeginUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318720"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="6597c-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="6597c-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="6597c-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="6597c-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="6597c-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="6597c-105">Remarks</span></span>

<span data-ttu-id="6597c-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6597c-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6597c-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6597c-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6597c-108">Se [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="6597c-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6597c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6597c-109">Requirements</span></span>



| <span data-ttu-id="6597c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6597c-110">Requirement</span></span> | <span data-ttu-id="6597c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6597c-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6597c-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6597c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6597c-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6597c-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6597c-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6597c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6597c-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6597c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6597c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6597c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6597c-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6597c-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6597c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="6597c-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6597c-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6597c-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6597c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6597c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6597c-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="6597c-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




