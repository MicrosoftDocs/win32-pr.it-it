---
description: 'Versione remota di IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233625"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="9bc0d-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="9bc0d-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="9bc0d-104">Versione remota di [**IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span><span class="sxs-lookup"><span data-stu-id="9bc0d-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="9bc0d-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bc0d-105">Remarks</span></span>

<span data-ttu-id="9bc0d-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9bc0d-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="9bc0d-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9bc0d-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="9bc0d-108">Se [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="9bc0d-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc0d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc0d-109">Requirements</span></span>



| <span data-ttu-id="9bc0d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc0d-110">Requirement</span></span> | <span data-ttu-id="9bc0d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc0d-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc0d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc0d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc0d-113">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9bc0d-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9bc0d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc0d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc0d-115">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9bc0d-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9bc0d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc0d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bc0d-117"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9bc0d-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc0d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bc0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc0d-119">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="9bc0d-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




