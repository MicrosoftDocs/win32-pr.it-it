---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7009def4e86a97720bc4b94eb2c9edb477afe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884678"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="20715-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="20715-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="20715-104">Versione utilizzabile del metodo [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="20715-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="20715-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="20715-105">Remarks</span></span>

<span data-ttu-id="20715-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="20715-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="20715-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="20715-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="20715-108">Se [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="20715-108">If [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="20715-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20715-109">Requirements</span></span>



| <span data-ttu-id="20715-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="20715-110">Requirement</span></span> | <span data-ttu-id="20715-111">Valore</span><span class="sxs-lookup"><span data-stu-id="20715-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20715-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20715-112">Minimum supported client</span></span><br/> | <span data-ttu-id="20715-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20715-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="20715-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20715-114">Minimum supported server</span></span><br/> | <span data-ttu-id="20715-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20715-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20715-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20715-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="20715-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20715-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="20715-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="20715-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="20715-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20715-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="20715-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20715-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20715-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="20715-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




