---
title: Proprietà UseMultimon di IMsRdpClientNonScriptable5
description: Specifica se il controllo ActiveX Desktop remoto deve usare più monitor.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà UseMultimon
- Servizi Desktop remoto proprietà UseMultimon, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà UseMultimon
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964508"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="42a95-106">Proprietà IMsRdpClientNonScriptable5:: UseMultimon</span><span class="sxs-lookup"><span data-stu-id="42a95-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="42a95-107">Specifica se il controllo ActiveX Desktop remoto deve usare più monitor.</span><span class="sxs-lookup"><span data-stu-id="42a95-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="42a95-108">Se questa proprietà contiene la **variante \_ true**, il controllo utilizzerà più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="42a95-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="42a95-109">Se questa proprietà contiene la **variante \_ false**, il controllo non utilizzerà più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="42a95-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="42a95-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="42a95-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a95-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42a95-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="42a95-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="42a95-112">Property value</span></span>

<span data-ttu-id="42a95-113">Specifica il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="42a95-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a95-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42a95-114">Requirements</span></span>



| <span data-ttu-id="42a95-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a95-115">Requirement</span></span> | <span data-ttu-id="42a95-116">Valore</span><span class="sxs-lookup"><span data-stu-id="42a95-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a95-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42a95-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42a95-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42a95-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="42a95-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42a95-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42a95-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42a95-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="42a95-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="42a95-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="42a95-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a95-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="42a95-123">DLL</span><span class="sxs-lookup"><span data-stu-id="42a95-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a95-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a95-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="42a95-125">IID</span><span class="sxs-lookup"><span data-stu-id="42a95-125">IID</span></span><br/>                      | <span data-ttu-id="42a95-126">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="42a95-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42a95-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42a95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a95-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="42a95-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





