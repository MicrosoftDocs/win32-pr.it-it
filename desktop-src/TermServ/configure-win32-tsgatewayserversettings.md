---
title: Metodo Configure della classe Win32_TSGatewayServerSettings
description: Configura le impostazioni RPC e IIS richieste dal servizio Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurare Servizi Desktop remoto del metodo
- Configurare Servizi Desktop remoto metodi, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo Configure
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1880e1a9811c8aab2660993c6c8ab05061163e1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048031"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="375f0-106">Metodo Configure della classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="375f0-106">Configure method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="375f0-107">Configura le impostazioni RPC e IIS richieste dal servizio Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="375f0-107">Configures the IIS and RPC settings required by the Remote Desktop Gateway (RD Gateway) service.</span></span>

## <a name="syntax"></a><span data-ttu-id="375f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="375f0-108">Syntax</span></span>


```mof
uint32 Configure();
```



## <a name="parameters"></a><span data-ttu-id="375f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="375f0-109">Parameters</span></span>

<span data-ttu-id="375f0-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="375f0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="375f0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="375f0-111">Return value</span></span>

<span data-ttu-id="375f0-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="375f0-112">Type: **uint32**</span></span>

<span data-ttu-id="375f0-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="375f0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="375f0-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="375f0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="375f0-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="375f0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="375f0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="375f0-116">Remarks</span></span>

<span data-ttu-id="375f0-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="375f0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="375f0-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="375f0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="375f0-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="375f0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="375f0-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="375f0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="375f0-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="375f0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="375f0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="375f0-122">Requirements</span></span>



| <span data-ttu-id="375f0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="375f0-123">Requirement</span></span> | <span data-ttu-id="375f0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="375f0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="375f0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="375f0-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="375f0-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="375f0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="375f0-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="375f0-128">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="375f0-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="375f0-129">Namespace</span></span><br/>                | <span data-ttu-id="375f0-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="375f0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="375f0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="375f0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="375f0-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="375f0-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="375f0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="375f0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="375f0-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="375f0-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="375f0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="375f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375f0-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="375f0-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

