---
title: Proprietà CmClassGuid di IMsRdpDeviceV2
description: Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CmClassGuid
- Servizi Desktop remoto proprietà CmClassGuid, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300991"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="df5d0-106">Proprietà IMsRdpDeviceV2:: CmClassGuid</span><span class="sxs-lookup"><span data-stu-id="df5d0-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="df5d0-107">Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df5d0-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="df5d0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="df5d0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df5d0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df5d0-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="df5d0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="df5d0-110">Property value</span></span>

<span data-ttu-id="df5d0-111">GUID della classe di installazione di Configuration Manager per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df5d0-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="df5d0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df5d0-112">Requirements</span></span>



| <span data-ttu-id="df5d0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="df5d0-113">Requirement</span></span> | <span data-ttu-id="df5d0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="df5d0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df5d0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df5d0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df5d0-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="df5d0-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="df5d0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df5d0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df5d0-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="df5d0-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="df5d0-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="df5d0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="df5d0-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df5d0-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df5d0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="df5d0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df5d0-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df5d0-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df5d0-123">IID</span><span class="sxs-lookup"><span data-stu-id="df5d0-123">IID</span></span><br/>                      | <span data-ttu-id="df5d0-124">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="df5d0-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="df5d0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df5d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5d0-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="df5d0-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





