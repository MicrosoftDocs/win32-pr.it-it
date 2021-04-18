---
description: 'Versione utilizzabile del metodo IMFMediaStream:: RequestSample.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309015"
---
# <a name="remoterequestsample"></a><span data-ttu-id="513ca-103">RemoteRequestSample</span><span class="sxs-lookup"><span data-stu-id="513ca-103">RemoteRequestSample</span></span>

<span data-ttu-id="513ca-104">Versione utilizzabile del metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="513ca-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="513ca-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="513ca-105">Remarks</span></span>

<span data-ttu-id="513ca-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="513ca-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="513ca-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="513ca-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="513ca-108">Se [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="513ca-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="513ca-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="513ca-109">Requirements</span></span>



| <span data-ttu-id="513ca-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="513ca-110">Requirement</span></span> | <span data-ttu-id="513ca-111">Valore</span><span class="sxs-lookup"><span data-stu-id="513ca-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513ca-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="513ca-112">Minimum supported client</span></span><br/> | <span data-ttu-id="513ca-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="513ca-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="513ca-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="513ca-114">Minimum supported server</span></span><br/> | <span data-ttu-id="513ca-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="513ca-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="513ca-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="513ca-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="513ca-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="513ca-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="513ca-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="513ca-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="513ca-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="513ca-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="513ca-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="513ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513ca-121">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="513ca-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




