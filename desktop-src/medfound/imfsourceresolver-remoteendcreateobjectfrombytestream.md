---
description: 'Versione utilizzabile del metodo IMFSourceResolver:: EndCreateObjectFromByteStream.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: RemoteEndCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130150"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="d083e-103">RemoteEndCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="d083e-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="d083e-104">Versione utilizzabile del metodo [**IMFSourceResolver:: EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="d083e-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="d083e-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="d083e-105">Remarks</span></span>

<span data-ttu-id="d083e-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d083e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d083e-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d083e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d083e-108">Se [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="d083e-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d083e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d083e-109">Requirements</span></span>



| <span data-ttu-id="d083e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d083e-110">Requirement</span></span> | <span data-ttu-id="d083e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d083e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d083e-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d083e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d083e-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d083e-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="d083e-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d083e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d083e-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d083e-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="d083e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d083e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d083e-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d083e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d083e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d083e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d083e-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d083e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d083e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d083e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d083e-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="d083e-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




