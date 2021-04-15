---
title: Proprietà GatewayEncryptedAuthCookieSize di IMsRdpClientTransportSettings3
description: Dimensione, in caratteri, della proprietà GatewayEncryptedAuthCookie.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayEncryptedAuthCookieSize
- Servizi Desktop remoto proprietà GatewayEncryptedAuthCookieSize, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayEncryptedAuthCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477440"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a><span data-ttu-id="4c169-106">Proprietà IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookieSize</span><span class="sxs-lookup"><span data-stu-id="4c169-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize property</span></span>

<span data-ttu-id="4c169-107">Dimensione, in caratteri, della proprietà [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="4c169-107">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span>

<span data-ttu-id="4c169-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4c169-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c169-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c169-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="4c169-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4c169-110">Property value</span></span>

<span data-ttu-id="4c169-111">Valore **ULONG** che contiene il nuovo valore di dimensione.</span><span class="sxs-lookup"><span data-stu-id="4c169-111">A **ULONG** value that contains the new size value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c169-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c169-112">Requirements</span></span>



| <span data-ttu-id="4c169-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c169-113">Requirement</span></span> | <span data-ttu-id="4c169-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4c169-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c169-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c169-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c169-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c169-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="4c169-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c169-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c169-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c169-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c169-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4c169-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c169-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c169-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c169-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4c169-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c169-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c169-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c169-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c169-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c169-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="4c169-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





