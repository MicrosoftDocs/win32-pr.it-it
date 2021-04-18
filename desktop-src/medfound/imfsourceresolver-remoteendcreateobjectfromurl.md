---
description: 'Versione utilizzabile del metodo IMFSourceResolver:: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308279"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="589c5-103">RemoteEndCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="589c5-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="589c5-104">Versione utilizzabile del metodo [**IMFSourceResolver:: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="589c5-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="589c5-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="589c5-105">Remarks</span></span>

<span data-ttu-id="589c5-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="589c5-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="589c5-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="589c5-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="589c5-108">Se [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="589c5-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="589c5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="589c5-109">Requirements</span></span>



| <span data-ttu-id="589c5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="589c5-110">Requirement</span></span> | <span data-ttu-id="589c5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="589c5-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589c5-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="589c5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="589c5-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="589c5-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="589c5-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="589c5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="589c5-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="589c5-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="589c5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="589c5-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="589c5-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="589c5-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="589c5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="589c5-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="589c5-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="589c5-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="589c5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="589c5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589c5-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="589c5-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




