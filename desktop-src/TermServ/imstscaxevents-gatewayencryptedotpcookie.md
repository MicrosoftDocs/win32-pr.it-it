---
title: Proprietà GatewayEncryptedOtpCookie di IMsRdpClientTransportSettings2
description: Specifica o Recupera il cookie crittografato per la password monouso (OTP).
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayEncryptedOtpCookie
- Servizi Desktop remoto proprietà GatewayEncryptedOtpCookie, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayEncryptedOtpCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519222"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="c16e9-106">Proprietà IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookie</span><span class="sxs-lookup"><span data-stu-id="c16e9-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="c16e9-107">Specifica o Recupera il cookie crittografato per la password monouso (OTP).</span><span class="sxs-lookup"><span data-stu-id="c16e9-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="c16e9-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c16e9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16e9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c16e9-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="c16e9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c16e9-110">Property value</span></span>

<span data-ttu-id="c16e9-111">Specifica o Recupera il cookie OTP crittografato.</span><span class="sxs-lookup"><span data-stu-id="c16e9-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="c16e9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c16e9-112">Requirements</span></span>



| <span data-ttu-id="c16e9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c16e9-113">Requirement</span></span> | <span data-ttu-id="c16e9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c16e9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16e9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16e9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c16e9-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c16e9-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="c16e9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16e9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c16e9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c16e9-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="c16e9-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c16e9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c16e9-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c16e9-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c16e9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c16e9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c16e9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c16e9-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c16e9-123">IID</span><span class="sxs-lookup"><span data-stu-id="c16e9-123">IID</span></span><br/>                      | <span data-ttu-id="c16e9-124">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="c16e9-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c16e9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c16e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16e9-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="c16e9-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="c16e9-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="c16e9-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





