---
title: Proprietà BandwidthDetection di IMsRdpClientAdvancedSettings8
description: Specifica se le modifiche della larghezza di banda vengono rilevate automaticamente.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BandwidthDetection
- Servizi Desktop remoto proprietà BandwidthDetection, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301222"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="60332-106">Proprietà IMsRdpClientAdvancedSettings8:: BandwidthDetection</span><span class="sxs-lookup"><span data-stu-id="60332-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="60332-107">Specifica se le modifiche della larghezza di banda vengono rilevate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="60332-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="60332-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="60332-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="60332-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60332-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="60332-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="60332-110">Property value</span></span>

<span data-ttu-id="60332-111">**Variante \_ TRUE** se le modifiche della larghezza di banda vengono rilevate automaticamente o **Variant \_ false** in alternativa.</span><span class="sxs-lookup"><span data-stu-id="60332-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="60332-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60332-112">Requirements</span></span>



| <span data-ttu-id="60332-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="60332-113">Requirement</span></span> | <span data-ttu-id="60332-114">Valore</span><span class="sxs-lookup"><span data-stu-id="60332-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60332-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60332-115">Minimum supported client</span></span><br/> | <span data-ttu-id="60332-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60332-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="60332-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60332-117">Minimum supported server</span></span><br/> | <span data-ttu-id="60332-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60332-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="60332-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="60332-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="60332-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60332-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="60332-121">DLL</span><span class="sxs-lookup"><span data-stu-id="60332-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60332-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60332-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60332-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60332-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60332-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="60332-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





