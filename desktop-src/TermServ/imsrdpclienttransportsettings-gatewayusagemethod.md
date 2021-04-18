---
title: Proprietà GatewayUsageMethod di IMsRdpClientTransportSettings
description: Specifica quando utilizzare un server Gateway Desktop remoto di Desktop remoto.
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayUsageMethod
- Servizi Desktop remoto proprietà GatewayUsageMethod, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301217"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="529c1-106">Proprietà IMsRdpClientTransportSettings:: GatewayUsageMethod</span><span class="sxs-lookup"><span data-stu-id="529c1-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="529c1-107">Specifica quando utilizzare un server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="529c1-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="529c1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="529c1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="529c1-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="529c1-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="529c1-110">Property value</span></span>

<span data-ttu-id="529c1-111">Variabile **ULONG** che specifica il metodo di utilizzo del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="529c1-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="529c1-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="529c1-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modalità proxy \_ Nessuna \_ diretta** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="529c1-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="529c1-114">Non usare un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="529c1-115">Nell'interfaccia utente del client Connessione Desktop remoto (RDC), la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** è deselezionata.</span><span class="sxs-lookup"><span data-stu-id="529c1-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="529c1-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modalità proxy \_ diretta** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="529c1-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="529c1-117">Usare sempre un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="529c1-118">Nell'interfaccia utente del client RDC, la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** è deselezionata.</span><span class="sxs-lookup"><span data-stu-id="529c1-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="529c1-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Rilevamento modalità proxy** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="529c1-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="529c1-120">Utilizzare un server Gateway Desktop remoto se non è possibile effettuare una connessione diretta al server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="529c1-121">Nell'interfaccia utente del client RDC è selezionata la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** .</span><span class="sxs-lookup"><span data-stu-id="529c1-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="529c1-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Impostazione predefinita modalità proxy** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="529c1-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="529c1-123">Utilizzare le impostazioni predefinite del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="529c1-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_ \_ \_ Rilevamento nessuna modalità proxy** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="529c1-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="529c1-125">Non usare un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="529c1-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="529c1-126">Nell'interfaccia utente del client RDC è selezionata la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** .</span><span class="sxs-lookup"><span data-stu-id="529c1-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="529c1-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="529c1-127">Error codes</span></span>

<span data-ttu-id="529c1-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="529c1-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="529c1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="529c1-129">Requirements</span></span>



| <span data-ttu-id="529c1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="529c1-130">Requirement</span></span> | <span data-ttu-id="529c1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="529c1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="529c1-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="529c1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="529c1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="529c1-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="529c1-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="529c1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="529c1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="529c1-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="529c1-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="529c1-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="529c1-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="529c1-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="529c1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="529c1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="529c1-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="529c1-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="529c1-140">IID</span><span class="sxs-lookup"><span data-stu-id="529c1-140">IID</span></span><br/>                      | <span data-ttu-id="529c1-141">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="529c1-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="529c1-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="529c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="529c1-143">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="529c1-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





