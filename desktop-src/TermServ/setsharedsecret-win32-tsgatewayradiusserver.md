---
title: Metodo SetSharedSecret della classe Win32_TSGatewayRADIUSServer
description: Imposta la proprietà SharedSecret per questo server Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSharedSecret
- Metodo SetSharedSecret Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742367"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="a3f30-106">Metodo SetSharedSecret della \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="a3f30-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="a3f30-107">Imposta la proprietà **SharedSecret** per questo server Remote Authentication Dial-in User Service (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="a3f30-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3f30-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="a3f30-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3f30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f30-110">*SharedSecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3f30-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f30-111">Nuovo segreto condiviso.</span><span class="sxs-lookup"><span data-stu-id="a3f30-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f30-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3f30-112">Return value</span></span>

<span data-ttu-id="a3f30-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a3f30-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a3f30-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a3f30-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a3f30-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a3f30-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f30-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3f30-116">Remarks</span></span>

<span data-ttu-id="a3f30-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="a3f30-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a3f30-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a3f30-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a3f30-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a3f30-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a3f30-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a3f30-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a3f30-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a3f30-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f30-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3f30-122">Requirements</span></span>



| <span data-ttu-id="a3f30-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f30-123">Requirement</span></span> | <span data-ttu-id="a3f30-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a3f30-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f30-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f30-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f30-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3f30-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a3f30-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f30-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f30-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f30-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a3f30-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3f30-129">Namespace</span></span><br/>                | <span data-ttu-id="a3f30-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a3f30-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a3f30-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a3f30-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3f30-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3f30-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3f30-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f30-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f30-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f30-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a3f30-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3f30-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f30-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a3f30-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

