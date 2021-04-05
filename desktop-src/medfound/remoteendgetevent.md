---
description: 'Versione utilizzabile del metodo IMFMediaEventGenerator:: EndGetEvent.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: RemoteEndGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753882"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="28e6a-103">RemoteEndGetEvent</span><span class="sxs-lookup"><span data-stu-id="28e6a-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="28e6a-104">Versione utilizzabile del metodo [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) .</span><span class="sxs-lookup"><span data-stu-id="28e6a-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="28e6a-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="28e6a-105">Remarks</span></span>

<span data-ttu-id="28e6a-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="28e6a-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="28e6a-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="28e6a-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="28e6a-108">Se [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="28e6a-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e6a-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28e6a-109">Requirements</span></span>



| <span data-ttu-id="28e6a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e6a-110">Requirement</span></span> | <span data-ttu-id="28e6a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="28e6a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e6a-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28e6a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="28e6a-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="28e6a-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="28e6a-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28e6a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="28e6a-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="28e6a-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="28e6a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28e6a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e6a-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28e6a-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="28e6a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="28e6a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="28e6a-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28e6a-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="28e6a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28e6a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e6a-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="28e6a-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




