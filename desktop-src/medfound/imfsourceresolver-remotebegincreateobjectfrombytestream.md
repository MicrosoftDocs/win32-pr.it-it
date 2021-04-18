---
description: 'Versione utilizzabile del metodo IMFSourceResolver:: BeginCreateObjectFromByteStream.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: RemoteBeginCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308477"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="620d6-103">RemoteBeginCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="620d6-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="620d6-104">Versione utilizzabile del metodo [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="620d6-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="620d6-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="620d6-105">Remarks</span></span>

<span data-ttu-id="620d6-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="620d6-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="620d6-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="620d6-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="620d6-108">Se [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="620d6-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="620d6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="620d6-109">Requirements</span></span>



| <span data-ttu-id="620d6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="620d6-110">Requirement</span></span> | <span data-ttu-id="620d6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="620d6-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620d6-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="620d6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="620d6-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="620d6-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="620d6-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="620d6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="620d6-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="620d6-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="620d6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="620d6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="620d6-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="620d6-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="620d6-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="620d6-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="620d6-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="620d6-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="620d6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="620d6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620d6-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="620d6-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




