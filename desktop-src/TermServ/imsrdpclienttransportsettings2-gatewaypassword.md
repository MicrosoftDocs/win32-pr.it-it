---
title: Proprietà GatewayPassword di IMsRdpClientTransportSettings2
description: Specifica la password fornita da un utente per la connessione al server Gateway Desktop remoto di Desktop remoto.
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPassword
- Servizi Desktop remoto proprietà GatewayPassword, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517487"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="dabcf-106">Proprietà IMsRdpClientTransportSettings2:: GatewayPassword</span><span class="sxs-lookup"><span data-stu-id="dabcf-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="dabcf-107">Specifica la password fornita da un utente per la connessione al server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="dabcf-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="dabcf-108">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="dabcf-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dabcf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dabcf-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="dabcf-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dabcf-110">Property value</span></span>

<span data-ttu-id="dabcf-111">Password fornita da un utente per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="dabcf-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dabcf-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="dabcf-112">Error codes</span></span>

<span data-ttu-id="dabcf-113">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dabcf-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="dabcf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dabcf-114">Requirements</span></span>



| <span data-ttu-id="dabcf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dabcf-115">Requirement</span></span> | <span data-ttu-id="dabcf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dabcf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dabcf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dabcf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dabcf-118">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="dabcf-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="dabcf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dabcf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dabcf-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dabcf-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="dabcf-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="dabcf-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="dabcf-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="dabcf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dabcf-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dabcf-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="dabcf-125">IID</span><span class="sxs-lookup"><span data-stu-id="dabcf-125">IID</span></span><br/>                      | <span data-ttu-id="dabcf-126">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="dabcf-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dabcf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dabcf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabcf-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="dabcf-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="dabcf-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="dabcf-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





