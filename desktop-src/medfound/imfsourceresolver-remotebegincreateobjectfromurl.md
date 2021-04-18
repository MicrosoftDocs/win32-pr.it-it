---
description: 'Versione utilizzabile del metodo IMFSourceResolver:: BeginCreateObjectFromURL.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: RemoteBeginCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308744"
---
# <a name="remotebegincreateobjectfromurl"></a><span data-ttu-id="e5c8d-103">RemoteBeginCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="e5c8d-103">RemoteBeginCreateObjectFromURL</span></span>

<span data-ttu-id="e5c8d-104">Versione utilizzabile del metodo [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="e5c8d-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="e5c8d-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5c8d-105">Remarks</span></span>

<span data-ttu-id="e5c8d-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="e5c8d-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="e5c8d-108">Se [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-108">If [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c8d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c8d-109">Requirements</span></span>



| <span data-ttu-id="e5c8d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c8d-110">Requirement</span></span> | <span data-ttu-id="e5c8d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c8d-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c8d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5c8d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c8d-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e5c8d-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="e5c8d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5c8d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c8d-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e5c8d-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="e5c8d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c8d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c8d-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c8d-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="e5c8d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5c8d-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5c8d-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5c8d-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e5c8d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c8d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c8d-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="e5c8d-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




