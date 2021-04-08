---
description: 'Versione utilizzabile del metodo IMFMediaEventGenerator:: BeginGetEvent.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: RemoteBeginGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880061"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="c69ea-103">RemoteBeginGetEvent</span><span class="sxs-lookup"><span data-stu-id="c69ea-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="c69ea-104">Versione utilizzabile del metodo [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) .</span><span class="sxs-lookup"><span data-stu-id="c69ea-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="c69ea-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="c69ea-105">Remarks</span></span>

<span data-ttu-id="c69ea-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c69ea-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c69ea-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c69ea-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c69ea-108">Se [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="c69ea-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c69ea-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c69ea-109">Requirements</span></span>



| <span data-ttu-id="c69ea-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69ea-110">Requirement</span></span> | <span data-ttu-id="c69ea-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c69ea-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c69ea-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c69ea-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c69ea-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c69ea-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c69ea-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c69ea-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c69ea-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c69ea-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c69ea-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c69ea-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c69ea-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c69ea-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c69ea-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c69ea-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c69ea-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c69ea-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c69ea-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c69ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69ea-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="c69ea-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




