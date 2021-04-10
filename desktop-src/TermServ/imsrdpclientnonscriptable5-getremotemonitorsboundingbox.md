---
title: Proprietà GetRemoteMonitorsBoundingBox di IMsRdpClientNonScriptable5
description: Specifica il rettangolo di delimitazione del monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GetRemoteMonitorsBoundingBox
- Servizi Desktop remoto proprietà GetRemoteMonitorsBoundingBox, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964509"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="dc21a-106">Proprietà IMsRdpClientNonScriptable5:: GetRemoteMonitorsBoundingBox</span><span class="sxs-lookup"><span data-stu-id="dc21a-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="dc21a-107">Specifica il rettangolo di delimitazione del monitor remoto.</span><span class="sxs-lookup"><span data-stu-id="dc21a-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="dc21a-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dc21a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc21a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc21a-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="dc21a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dc21a-110">Property value</span></span>

<span data-ttu-id="dc21a-111">Riceve il bordo sinistro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="dc21a-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="dc21a-112">Riceve il bordo superiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="dc21a-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="dc21a-113">Riceve il bordo destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="dc21a-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="dc21a-114">Riceve il bordo inferiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="dc21a-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc21a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc21a-115">Remarks</span></span>

<span data-ttu-id="dc21a-116">Tutte le coordinate si trovano nelle coordinate dello schermo virtuale, che sono relative all'angolo superiore sinistro del monitor primario.</span><span class="sxs-lookup"><span data-stu-id="dc21a-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="dc21a-117">Se non si tratta del monitoraggio principale, alcuni o tutti questi valori potrebbero essere negativi.</span><span class="sxs-lookup"><span data-stu-id="dc21a-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc21a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc21a-118">Requirements</span></span>



| <span data-ttu-id="dc21a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc21a-119">Requirement</span></span> | <span data-ttu-id="dc21a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dc21a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc21a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc21a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc21a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc21a-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dc21a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc21a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc21a-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc21a-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="dc21a-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="dc21a-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc21a-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dc21a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dc21a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc21a-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dc21a-129">IID</span><span class="sxs-lookup"><span data-stu-id="dc21a-129">IID</span></span><br/>                      | <span data-ttu-id="dc21a-130">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="dc21a-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc21a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc21a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc21a-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="dc21a-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





