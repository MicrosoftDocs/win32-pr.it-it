---
title: Proprietà GatewayIsSupported di IMsRdpClientTransportSettings
description: Specifica se Desktop remoto Gateway Desktop remoto è supportato.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayIsSupported
- Servizi Desktop remoto proprietà GatewayIsSupported, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400237"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="e20d9-106">Proprietà IMsRdpClientTransportSettings:: GatewayIsSupported</span><span class="sxs-lookup"><span data-stu-id="e20d9-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="e20d9-107">Specifica se Desktop remoto Gateway Desktop remoto è supportato.</span><span class="sxs-lookup"><span data-stu-id="e20d9-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="e20d9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e20d9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20d9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e20d9-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="e20d9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e20d9-110">Property value</span></span>

<span data-ttu-id="e20d9-111">Specifica se Gateway Desktop remoto è supportato.</span><span class="sxs-lookup"><span data-stu-id="e20d9-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e20d9-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e20d9-112">Error codes</span></span>

<span data-ttu-id="e20d9-113">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e20d9-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e20d9-114">Requirements</span></span>



| <span data-ttu-id="e20d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e20d9-115">Requirement</span></span> | <span data-ttu-id="e20d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e20d9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e20d9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e20d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e20d9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e20d9-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e20d9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e20d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e20d9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e20d9-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e20d9-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e20d9-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e20d9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e20d9-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e20d9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e20d9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e20d9-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e20d9-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e20d9-125">IID</span><span class="sxs-lookup"><span data-stu-id="e20d9-125">IID</span></span><br/>                      | <span data-ttu-id="e20d9-126">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="e20d9-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e20d9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e20d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20d9-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e20d9-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





