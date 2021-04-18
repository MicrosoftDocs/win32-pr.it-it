---
title: Proprietà GatewayUserName di IMsRdpClientTransportSettings2
description: Specifica o Recupera il nome utente fornito al server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayUserName
- Servizi Desktop remoto proprietà GatewayUserName, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301215"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="b560a-106">Proprietà IMsRdpClientTransportSettings2:: GatewayUserName</span><span class="sxs-lookup"><span data-stu-id="b560a-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="b560a-107">Specifica o Recupera il nome utente fornito al server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="b560a-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="b560a-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b560a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b560a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b560a-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="b560a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b560a-110">Property value</span></span>

<span data-ttu-id="b560a-111">Nome utente fornito per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b560a-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b560a-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b560a-112">Error codes</span></span>

<span data-ttu-id="b560a-113">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b560a-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b560a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b560a-114">Requirements</span></span>



| <span data-ttu-id="b560a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b560a-115">Requirement</span></span> | <span data-ttu-id="b560a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b560a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b560a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b560a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b560a-118">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="b560a-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="b560a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b560a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b560a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b560a-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="b560a-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b560a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b560a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b560a-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="b560a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b560a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b560a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b560a-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="b560a-125">IID</span><span class="sxs-lookup"><span data-stu-id="b560a-125">IID</span></span><br/>                      | <span data-ttu-id="b560a-126">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="b560a-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b560a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b560a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b560a-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="b560a-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="b560a-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="b560a-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





