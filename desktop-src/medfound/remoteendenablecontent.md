---
description: 'Versione utilizzabile del metodo IMFContentProtectionManager:: EndEnableContent.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: RemoteEndEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880058"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="93ddc-103">RemoteEndEnableContent</span><span class="sxs-lookup"><span data-stu-id="93ddc-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="93ddc-104">Versione utilizzabile del metodo [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="93ddc-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="93ddc-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="93ddc-105">Remarks</span></span>

<span data-ttu-id="93ddc-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="93ddc-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="93ddc-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="93ddc-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="93ddc-108">Se [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="93ddc-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ddc-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93ddc-109">Requirements</span></span>



| <span data-ttu-id="93ddc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ddc-110">Requirement</span></span> | <span data-ttu-id="93ddc-111">Valore</span><span class="sxs-lookup"><span data-stu-id="93ddc-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ddc-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ddc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="93ddc-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93ddc-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93ddc-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ddc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="93ddc-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93ddc-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93ddc-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93ddc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ddc-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93ddc-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="93ddc-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="93ddc-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="93ddc-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93ddc-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="93ddc-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93ddc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ddc-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="93ddc-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




