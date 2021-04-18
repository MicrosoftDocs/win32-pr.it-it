---
description: 'Versione utilizzabile del metodo IMFContentProtectionManager:: BeginEnableContent.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: RemoteBeginEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309018"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="99821-103">RemoteBeginEnableContent</span><span class="sxs-lookup"><span data-stu-id="99821-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="99821-104">Versione utilizzabile del metodo [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="99821-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="99821-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="99821-105">Remarks</span></span>

<span data-ttu-id="99821-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="99821-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="99821-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99821-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="99821-108">Se [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="99821-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="99821-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99821-109">Requirements</span></span>



| <span data-ttu-id="99821-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="99821-110">Requirement</span></span> | <span data-ttu-id="99821-111">Valore</span><span class="sxs-lookup"><span data-stu-id="99821-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99821-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99821-112">Minimum supported client</span></span><br/> | <span data-ttu-id="99821-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99821-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99821-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99821-114">Minimum supported server</span></span><br/> | <span data-ttu-id="99821-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99821-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99821-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99821-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="99821-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99821-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="99821-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="99821-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="99821-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99821-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="99821-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99821-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99821-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="99821-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




