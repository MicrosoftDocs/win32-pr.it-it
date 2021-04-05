---
description: 'Versione utilizzabile del metodo IMFTopologyNode:: GetInputPrefType.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: RemoteGetInputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752887"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="c57ce-103">RemoteGetInputPrefType</span><span class="sxs-lookup"><span data-stu-id="c57ce-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="c57ce-104">Versione utilizzabile del metodo [**IMFTopologyNode:: GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="c57ce-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="c57ce-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="c57ce-105">Remarks</span></span>

<span data-ttu-id="c57ce-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c57ce-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c57ce-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c57ce-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c57ce-108">Se [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="c57ce-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57ce-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c57ce-109">Requirements</span></span>



| <span data-ttu-id="c57ce-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c57ce-110">Requirement</span></span> | <span data-ttu-id="c57ce-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c57ce-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ce-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c57ce-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c57ce-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c57ce-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c57ce-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c57ce-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c57ce-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c57ce-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c57ce-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c57ce-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57ce-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c57ce-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c57ce-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c57ce-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c57ce-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c57ce-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c57ce-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c57ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57ce-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c57ce-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




