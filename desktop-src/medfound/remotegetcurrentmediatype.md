---
description: 'Versione utilizzabile del metodo IMFMediaTypeHandler:: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320482"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="400ef-103">RemoteGetCurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="400ef-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="400ef-104">Versione utilizzabile del metodo [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="400ef-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="400ef-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="400ef-105">Remarks</span></span>

<span data-ttu-id="400ef-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="400ef-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="400ef-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="400ef-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="400ef-108">Se [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="400ef-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="400ef-109">Questa interfaccia è disponibile nelle piattaforme seguenti se sono installati i componenti ridistribuibili di Windows Media Format 11 SDK:</span><span class="sxs-lookup"><span data-stu-id="400ef-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="400ef-110">Windows XP con Service Pack 2 (SP2) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="400ef-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="400ef-111">Windows XP Media Center Edition 2005 con KB900325 (Windows XP Media Center Edition 2005) e KB925766 (aggiornamento cumulativo ottobre 2006 per Windows XP Media Center Edition) installato.</span><span class="sxs-lookup"><span data-stu-id="400ef-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="400ef-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="400ef-112">Requirements</span></span>



| <span data-ttu-id="400ef-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="400ef-113">Requirement</span></span> | <span data-ttu-id="400ef-114">Valore</span><span class="sxs-lookup"><span data-stu-id="400ef-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="400ef-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="400ef-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="400ef-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="400ef-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="400ef-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="400ef-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="400ef-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="400ef-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="400ef-120"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="400ef-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="400ef-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="400ef-122"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="400ef-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="400ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400ef-124">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="400ef-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




