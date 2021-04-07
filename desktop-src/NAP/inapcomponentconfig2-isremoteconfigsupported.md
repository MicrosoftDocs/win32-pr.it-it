---
title: Metodo INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per indicare se la configurazione remota è supportata.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- NAP metodo IsRemoteConfigSupported
- Metodo IsRemoteConfigSupported NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964015"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="76123-106">Metodo INapComponentConfig2:: IsRemoteConfigSupported</span><span class="sxs-lookup"><span data-stu-id="76123-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="76123-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="76123-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="76123-108">Il metodo **IsRemoteConfigSupported** viene implementato da convalida integrità sistema (SHV) per indicare se la configurazione remota è supportata.</span><span class="sxs-lookup"><span data-stu-id="76123-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="76123-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76123-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="76123-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="76123-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76123-111">*supportato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76123-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76123-112">Puntatore a un BOOL che è impostato su **true** se il componente supporta la configurazione remota e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="76123-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="76123-113">*remoteConfigType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76123-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76123-114">Indica il tipo di configurazione remota supportato usando il valore dell'enumerazione [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :</span><span class="sxs-lookup"><span data-stu-id="76123-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="76123-115">Valore</span><span class="sxs-lookup"><span data-stu-id="76123-115">Value</span></span>                                                                                                 | <span data-ttu-id="76123-116">Significato</span><span class="sxs-lookup"><span data-stu-id="76123-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76123-117"><dt>remoteConfigTypeMachine</dt></span><span class="sxs-lookup"><span data-stu-id="76123-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="76123-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) è implementato.</span><span class="sxs-lookup"><span data-stu-id="76123-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="76123-119"><dt>remoteConfigTypeConfigBlob</dt></span><span class="sxs-lookup"><span data-stu-id="76123-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="76123-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) è implementato.</span><span class="sxs-lookup"><span data-stu-id="76123-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="76123-121">[**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig:: Seconfig**](inapcomponentconfig-setconfig.md) possono essere chiamati in remoto mediante DCOM.</span><span class="sxs-lookup"><span data-stu-id="76123-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76123-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76123-122">Return value</span></span>

<span data-ttu-id="76123-123">Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="76123-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="76123-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="76123-124">Remarks</span></span>

<span data-ttu-id="76123-125">Se non viene implementato né [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) né [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) , non è possibile configurare in remoto il servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="76123-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="76123-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76123-126">Requirements</span></span>



| <span data-ttu-id="76123-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="76123-127">Requirement</span></span> | <span data-ttu-id="76123-128">Valore</span><span class="sxs-lookup"><span data-stu-id="76123-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76123-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76123-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76123-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76123-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="76123-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76123-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76123-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76123-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76123-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76123-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="76123-134"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="76123-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="76123-135">IDL</span><span class="sxs-lookup"><span data-stu-id="76123-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76123-136"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76123-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76123-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76123-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76123-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="76123-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





