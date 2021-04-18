---
description: 'Versione utilizzabile del metodo IMFTopologyNode:: GetOutputPrefType.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: RemoteGetOutputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308474"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="3d183-103">RemoteGetOutputPrefType</span><span class="sxs-lookup"><span data-stu-id="3d183-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="3d183-104">Versione utilizzabile del metodo [**IMFTopologyNode:: GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="3d183-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="3d183-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d183-105">Remarks</span></span>

<span data-ttu-id="3d183-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3d183-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3d183-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3d183-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3d183-108">Se **GetOutputPrefType** viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="3d183-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d183-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d183-109">Requirements</span></span>



| <span data-ttu-id="3d183-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d183-110">Requirement</span></span> | <span data-ttu-id="3d183-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3d183-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d183-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d183-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3d183-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d183-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d183-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d183-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3d183-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d183-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d183-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d183-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d183-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d183-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d183-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d183-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d183-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d183-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3d183-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d183-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d183-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3d183-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




