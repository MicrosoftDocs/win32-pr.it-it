---
title: Proprietà GatewayUserSelectedCredsSource di IMsRdpClientTransportSettings
description: Imposta o recupera l'origine della credenziale del Gateway Desktop remoto specificata dall'utente Desktop remoto.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayUserSelectedCredsSource
- Servizi Desktop remoto proprietà GatewayUserSelectedCredsSource, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517488"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="935fd-106">Proprietà IMsRdpClientTransportSettings:: GatewayUserSelectedCredsSource</span><span class="sxs-lookup"><span data-stu-id="935fd-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="935fd-107">Imposta o recupera l'origine della credenziale del Gateway Desktop remoto specificata dall'utente Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="935fd-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="935fd-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="935fd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="935fd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="935fd-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="935fd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="935fd-110">Property value</span></span>

<span data-ttu-id="935fd-111">Variabile **ULONG** che specifica il metodo di autenticazione Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="935fd-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="935fd-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="935fd-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="935fd-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ \_Modalità credenziali \_ proxy \_ USERPASS** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="935fd-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="935fd-114">Usare una password (NTLM) come metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="935fd-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="935fd-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ Smart Card in modalità credenziali proxy** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="935fd-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="935fd-116">Usare una smart card come metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="935fd-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="935fd-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ \_Modalità credenziali \_ proxy \_ any** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="935fd-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="935fd-118">Usare qualsiasi metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="935fd-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="935fd-119">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="935fd-119">Error codes</span></span>

<span data-ttu-id="935fd-120">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="935fd-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="935fd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="935fd-121">Requirements</span></span>



| <span data-ttu-id="935fd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="935fd-122">Requirement</span></span> | <span data-ttu-id="935fd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="935fd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935fd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="935fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="935fd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="935fd-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="935fd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="935fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="935fd-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="935fd-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="935fd-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="935fd-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="935fd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935fd-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="935fd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="935fd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="935fd-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935fd-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="935fd-132">IID</span><span class="sxs-lookup"><span data-stu-id="935fd-132">IID</span></span><br/>                      | <span data-ttu-id="935fd-133">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="935fd-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="935fd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="935fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935fd-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="935fd-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





