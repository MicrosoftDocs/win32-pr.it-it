---
title: Proprietà PublicMode di IMsRdpClientShell
description: Specifica o recupera se la modalità pubblica è abilitata.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, proprietà PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477759"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="1c8f8-106">IMsRdpClientShell::P proprietà ublicMode</span><span class="sxs-lookup"><span data-stu-id="1c8f8-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="1c8f8-107">Specifica o recupera se la modalità pubblica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1c8f8-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="1c8f8-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1c8f8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c8f8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c8f8-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="1c8f8-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1c8f8-110">Property value</span></span>

<span data-ttu-id="1c8f8-111">Specifica se la modalità pubblica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1c8f8-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c8f8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c8f8-112">Requirements</span></span>



| <span data-ttu-id="1c8f8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c8f8-113">Requirement</span></span> | <span data-ttu-id="1c8f8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1c8f8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8f8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c8f8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1c8f8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8f8-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c8f8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c8f8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1c8f8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c8f8-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c8f8-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1c8f8-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c8f8-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c8f8-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c8f8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1c8f8-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c8f8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c8f8-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c8f8-123">IID</span><span class="sxs-lookup"><span data-stu-id="1c8f8-123">IID</span></span><br/>                      | <span data-ttu-id="1c8f8-124">IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="1c8f8-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="1c8f8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c8f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c8f8-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="1c8f8-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





