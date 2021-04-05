---
title: Proprietà GatewayEncryptedOtpCookieSize di IMsRdpClientTransportSettings2
description: Specifica o recupera le dimensioni del cookie di password monouso (OTP) crittografato.
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayEncryptedOtpCookieSize
- Servizi Desktop remoto proprietà GatewayEncryptedOtpCookieSize, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayEncryptedOtpCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741338"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="bb373-106">Proprietà IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookieSize</span><span class="sxs-lookup"><span data-stu-id="bb373-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="bb373-107">Specifica o recupera le dimensioni del cookie di password monouso (OTP) crittografato.</span><span class="sxs-lookup"><span data-stu-id="bb373-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="bb373-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bb373-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb373-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb373-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="bb373-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb373-110">Property value</span></span>

<span data-ttu-id="bb373-111">Specifica o recupera le dimensioni del cookie di password monouso (OTP) crittografato.</span><span class="sxs-lookup"><span data-stu-id="bb373-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb373-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb373-112">Requirements</span></span>



| <span data-ttu-id="bb373-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb373-113">Requirement</span></span> | <span data-ttu-id="bb373-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bb373-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb373-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb373-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bb373-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="bb373-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="bb373-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb373-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bb373-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb373-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="bb373-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bb373-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb373-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb373-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bb373-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bb373-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb373-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb373-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bb373-123">IID</span><span class="sxs-lookup"><span data-stu-id="bb373-123">IID</span></span><br/>                      | <span data-ttu-id="bb373-124">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="bb373-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb373-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb373-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb373-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="bb373-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="bb373-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="bb373-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





