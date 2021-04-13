---
title: Proprietà DisableConnectionBar di IMsRdpClientNonScriptable5
description: Specifica se il controllo ActiveX Desktop remoto deve disabilitare la barra di connessione.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisableConnectionBar
- Servizi Desktop remoto proprietà DisableConnectionBar, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519237"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="9d93e-106">IMsRdpClientNonScriptable5::D Proprietà isableConnectionBar</span><span class="sxs-lookup"><span data-stu-id="9d93e-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="9d93e-107">Specifica se il controllo ActiveX Desktop remoto deve disabilitare la barra di connessione.</span><span class="sxs-lookup"><span data-stu-id="9d93e-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="9d93e-108">Se questa proprietà contiene la **variante \_ true**, la barra di connessione deve essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9d93e-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="9d93e-109">Se questa proprietà contiene la **variante \_ false**, la barra di connessione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="9d93e-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="9d93e-110">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="9d93e-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d93e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d93e-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="9d93e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d93e-112">Property value</span></span>

<span data-ttu-id="9d93e-113">Specifica il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d93e-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d93e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d93e-114">Requirements</span></span>



| <span data-ttu-id="9d93e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d93e-115">Requirement</span></span> | <span data-ttu-id="9d93e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9d93e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d93e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d93e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d93e-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d93e-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9d93e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d93e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d93e-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d93e-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="9d93e-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9d93e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d93e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d93e-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9d93e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9d93e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d93e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d93e-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9d93e-125">IID</span><span class="sxs-lookup"><span data-stu-id="9d93e-125">IID</span></span><br/>                      | <span data-ttu-id="9d93e-126">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="9d93e-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d93e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d93e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d93e-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="9d93e-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





