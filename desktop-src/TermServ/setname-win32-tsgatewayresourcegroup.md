---
title: Metodo Sename della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Name per il gruppo di risorse.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- Metodo senamer Servizi Desktop remoto
- Metodo senamer Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo SetValue
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873809"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="5d0b3-106">Metodo Sename della classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d0b3-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="5d0b3-107">Imposta la proprietà **Name** per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0b3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d0b3-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="5d0b3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d0b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d0b3-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d0b3-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d0b3-111">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-111">Name of the resource group.</span></span> <span data-ttu-id="5d0b3-112">Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:</span><span class="sxs-lookup"><span data-stu-id="5d0b3-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="5d0b3-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="5d0b3-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="5d0b3-114">\*\[Scheda\]</span><span class="sxs-lookup"><span data-stu-id="5d0b3-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d0b3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d0b3-115">Return value</span></span>

<span data-ttu-id="5d0b3-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5d0b3-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5d0b3-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5d0b3-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0b3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d0b3-119">Remarks</span></span>

<span data-ttu-id="5d0b3-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5d0b3-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5d0b3-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d0b3-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5d0b3-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5d0b3-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d0b3-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5d0b3-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0b3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d0b3-125">Requirements</span></span>



| <span data-ttu-id="5d0b3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d0b3-126">Requirement</span></span> | <span data-ttu-id="5d0b3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5d0b3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0b3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d0b3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0b3-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5d0b3-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5d0b3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d0b3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0b3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d0b3-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5d0b3-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d0b3-132">Namespace</span></span><br/>                | <span data-ttu-id="5d0b3-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5d0b3-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5d0b3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5d0b3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d0b3-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d0b3-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d0b3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5d0b3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d0b3-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d0b3-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5d0b3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d0b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0b3-139">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="5d0b3-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

