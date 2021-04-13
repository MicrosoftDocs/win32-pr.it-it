---
title: Proprietà GatewayHostname di IMsRdpClientTransportSettings
description: Specifica il nome host del server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayHostname
- Servizi Desktop remoto proprietà GatewayHostname, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340443"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="81a4a-106">Proprietà IMsRdpClientTransportSettings:: GatewayHostname</span><span class="sxs-lookup"><span data-stu-id="81a4a-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="81a4a-107">Specifica il nome host del server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="81a4a-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="81a4a-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="81a4a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a4a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81a4a-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="81a4a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="81a4a-110">Property value</span></span>

<span data-ttu-id="81a4a-111">Stringa che contiene il nome host del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="81a4a-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81a4a-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="81a4a-112">Error codes</span></span>

<span data-ttu-id="81a4a-113">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81a4a-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a4a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81a4a-114">Requirements</span></span>



| <span data-ttu-id="81a4a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a4a-115">Requirement</span></span> | <span data-ttu-id="81a4a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="81a4a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a4a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81a4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81a4a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81a4a-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="81a4a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81a4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81a4a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81a4a-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="81a4a-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="81a4a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="81a4a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a4a-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="81a4a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="81a4a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a4a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a4a-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="81a4a-125">IID</span><span class="sxs-lookup"><span data-stu-id="81a4a-125">IID</span></span><br/>                      | <span data-ttu-id="81a4a-126">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="81a4a-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81a4a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81a4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a4a-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="81a4a-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





