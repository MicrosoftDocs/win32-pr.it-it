---
description: 'Versione utilizzabile del metodo IMFMediaSource:: CreatePresentationDescriptor.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: RemoteCreatePresentationDescriptor (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130482"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="0db31-103">RemoteCreatePresentationDescriptor</span><span class="sxs-lookup"><span data-stu-id="0db31-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="0db31-104">Versione utilizzabile del metodo [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="0db31-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="0db31-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="0db31-105">Remarks</span></span>

<span data-ttu-id="0db31-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0db31-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="0db31-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0db31-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="0db31-108">Se [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="0db31-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db31-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0db31-109">Requirements</span></span>



| <span data-ttu-id="0db31-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db31-110">Requirement</span></span> | <span data-ttu-id="0db31-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0db31-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db31-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db31-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0db31-113">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0db31-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="0db31-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db31-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0db31-115">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0db31-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="0db31-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0db31-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db31-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0db31-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0db31-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="0db31-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0db31-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0db31-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0db31-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0db31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db31-121">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="0db31-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




