---
title: Metodo sedescription della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Description per il gruppo di risorse.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di descrizione
- Metodo sedescription Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo sedescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302595"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="10d62-106">Metodo sedescription della classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10d62-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="10d62-107">Imposta la proprietà **Description** per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10d62-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10d62-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="10d62-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="10d62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d62-110">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="10d62-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d62-111">Descrizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10d62-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10d62-112">Return value</span></span>

<span data-ttu-id="10d62-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="10d62-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="10d62-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="10d62-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="10d62-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10d62-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10d62-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="10d62-116">Remarks</span></span>

<span data-ttu-id="10d62-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="10d62-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="10d62-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10d62-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10d62-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="10d62-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10d62-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="10d62-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10d62-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10d62-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10d62-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10d62-122">Requirements</span></span>



| <span data-ttu-id="10d62-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d62-123">Requirement</span></span> | <span data-ttu-id="10d62-124">Valore</span><span class="sxs-lookup"><span data-stu-id="10d62-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d62-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="10d62-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10d62-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="10d62-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="10d62-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d62-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="10d62-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10d62-129">Namespace</span></span><br/>                | <span data-ttu-id="10d62-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="10d62-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="10d62-131">MOF</span><span class="sxs-lookup"><span data-stu-id="10d62-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10d62-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10d62-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="10d62-133">DLL</span><span class="sxs-lookup"><span data-stu-id="10d62-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d62-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d62-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="10d62-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10d62-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d62-136">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="10d62-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

