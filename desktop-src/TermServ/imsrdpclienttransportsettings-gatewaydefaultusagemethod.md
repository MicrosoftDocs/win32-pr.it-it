---
title: Proprietà GatewayDefaultUsageMethod di IMsRdpClientTransportSettings
description: Metodo di utilizzo predefinito per Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayDefaultUsageMethod
- Servizi Desktop remoto proprietà GatewayDefaultUsageMethod, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301219"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="ba7ea-106">Proprietà IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod</span><span class="sxs-lookup"><span data-stu-id="ba7ea-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="ba7ea-107">Metodo di utilizzo predefinito per Desktop remoto Gateway (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="ba7ea-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="ba7ea-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ba7ea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7ea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba7ea-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="ba7ea-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ba7ea-110">Property value</span></span>

<span data-ttu-id="ba7ea-111">Puntatore al metodo di utilizzo predefinito per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ba7ea-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="ba7ea-112">Restituisce un'Unione delle impostazioni utente impostate mediante [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)e le impostazioni di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ba7ea-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="ba7ea-113">Se non sono state impostate impostazioni utente mediante **put \_ GatewayUsageMethod ()**, **get \_ GatewayDefaultUsageMethod ()** restituirà il valore predefinito **della \_ modalità proxy TSC \_ \_ Detect**.</span><span class="sxs-lookup"><span data-stu-id="ba7ea-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba7ea-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba7ea-114">Error codes</span></span>

<span data-ttu-id="ba7ea-115">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ba7ea-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7ea-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba7ea-116">Requirements</span></span>



| <span data-ttu-id="ba7ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba7ea-117">Requirement</span></span> | <span data-ttu-id="ba7ea-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ba7ea-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7ea-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba7ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7ea-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba7ea-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ba7ea-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba7ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7ea-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba7ea-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ba7ea-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ba7ea-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba7ea-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7ea-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba7ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7ea-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7ea-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba7ea-127">IID</span><span class="sxs-lookup"><span data-stu-id="ba7ea-127">IID</span></span><br/>                      | <span data-ttu-id="ba7ea-128">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="ba7ea-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba7ea-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba7ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7ea-130">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="ba7ea-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





