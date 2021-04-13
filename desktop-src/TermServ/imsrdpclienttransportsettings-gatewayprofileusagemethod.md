---
title: Proprietà GatewayProfileUsageMethod di IMsRdpClientTransportSettings
description: Specifica se utilizzare le impostazioni predefinite del Gateway Desktop remoto Gateway.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayProfileUsageMethod
- Servizi Desktop remoto proprietà GatewayProfileUsageMethod, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400587"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="572b0-106">Proprietà IMsRdpClientTransportSettings:: GatewayProfileUsageMethod</span><span class="sxs-lookup"><span data-stu-id="572b0-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="572b0-107">Specifica se utilizzare le impostazioni predefinite del Gateway Desktop remoto Gateway.</span><span class="sxs-lookup"><span data-stu-id="572b0-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="572b0-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="572b0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="572b0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="572b0-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="572b0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="572b0-110">Property value</span></span>

<span data-ttu-id="572b0-111">Metodo di utilizzo del profilo Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="572b0-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="572b0-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="572b0-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="572b0-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ \_ \_ \_ Impostazione predefinita modalità profilo proxy** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="572b0-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="572b0-114">Utilizzare la modalità predefinita del profilo, come specificato dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="572b0-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="572b0-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ \_Modalità profilo \_ proxy \_ esplicita** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="572b0-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="572b0-116">Utilizzare le impostazioni esplicite, come specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="572b0-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="572b0-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="572b0-117">Error codes</span></span>

<span data-ttu-id="572b0-118">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="572b0-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="572b0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="572b0-119">Requirements</span></span>



| <span data-ttu-id="572b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="572b0-120">Requirement</span></span> | <span data-ttu-id="572b0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="572b0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="572b0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="572b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="572b0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="572b0-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="572b0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="572b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="572b0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="572b0-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="572b0-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="572b0-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="572b0-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="572b0-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="572b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="572b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="572b0-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="572b0-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="572b0-130">IID</span><span class="sxs-lookup"><span data-stu-id="572b0-130">IID</span></span><br/>                      | <span data-ttu-id="572b0-131">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="572b0-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="572b0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="572b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572b0-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="572b0-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





