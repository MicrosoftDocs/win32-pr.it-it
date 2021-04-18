---
title: Enumerazione ClientSpec
description: Utilizzato con la proprietà ClientProtocolSpec per specificare il protocollo desktop remoto utilizzato tra il client e il server.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301133"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="04f15-104">Enumerazione ClientSpec</span><span class="sxs-lookup"><span data-stu-id="04f15-104">ClientSpec enumeration</span></span>

<span data-ttu-id="04f15-105">Utilizzato con la proprietà [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) per specificare il protocollo desktop remoto utilizzato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="04f15-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f15-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04f15-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="04f15-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="04f15-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="04f15-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span><span class="sxs-lookup"><span data-stu-id="04f15-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="04f15-109">Il protocollo è il protocollo completo di Windows 8 Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="04f15-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="04f15-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span><span class="sxs-lookup"><span data-stu-id="04f15-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="04f15-111">Il protocollo è limitato all'uso del codec Windows 7 con SP1 RemoteFX e di una cache più piccola.</span><span class="sxs-lookup"><span data-stu-id="04f15-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="04f15-112">Tutti gli altri codec sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="04f15-112">All other codecs are disabled.</span></span> <span data-ttu-id="04f15-113">Questo protocollo ha il footprint di memoria più piccolo.</span><span class="sxs-lookup"><span data-stu-id="04f15-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="04f15-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span><span class="sxs-lookup"><span data-stu-id="04f15-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="04f15-115">Il protocollo è identico a **FullMode**, con la differenza che usa una cache più piccola.</span><span class="sxs-lookup"><span data-stu-id="04f15-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04f15-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04f15-116">Requirements</span></span>



| <span data-ttu-id="04f15-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04f15-117">Requirement</span></span> | <span data-ttu-id="04f15-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04f15-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04f15-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f15-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04f15-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04f15-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="04f15-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f15-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04f15-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04f15-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="04f15-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="04f15-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="04f15-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04f15-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f15-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04f15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f15-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span><span class="sxs-lookup"><span data-stu-id="04f15-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





