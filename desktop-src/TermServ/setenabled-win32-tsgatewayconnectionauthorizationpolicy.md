---
title: Metodo seenabled della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà Enabled, che Abilita o Disabilita i criteri di autorizzazione della connessione di Servizi Desktop remoto correnti (RD \ 160; LIMITE).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Metodo seenabled Servizi Desktop remoto
- Metodo seenabled Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo seenabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517691"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="aef56-106">Metodo seenabled della classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="aef56-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="aef56-107">Imposta la proprietà **Enabled** , che Abilita o Disabilita il criterio di autorizzazione di connessione del Servizi Desktop remoto corrente.</span><span class="sxs-lookup"><span data-stu-id="aef56-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="aef56-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aef56-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="aef56-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aef56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef56-110">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aef56-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aef56-111">**True** se il criterio di autorizzazione connessioni Desktop remoto deve essere abilitato, **false** se il CAP Rd deve essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="aef56-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef56-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aef56-112">Return value</span></span>

<span data-ttu-id="aef56-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="aef56-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="aef56-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="aef56-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="aef56-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aef56-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aef56-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aef56-116">Remarks</span></span>

<span data-ttu-id="aef56-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="aef56-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="aef56-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aef56-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aef56-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="aef56-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aef56-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="aef56-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aef56-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aef56-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aef56-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aef56-122">Requirements</span></span>



| <span data-ttu-id="aef56-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef56-123">Requirement</span></span> | <span data-ttu-id="aef56-124">Valore</span><span class="sxs-lookup"><span data-stu-id="aef56-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef56-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef56-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aef56-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="aef56-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="aef56-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef56-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aef56-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aef56-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aef56-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aef56-129">Namespace</span></span><br/>                | <span data-ttu-id="aef56-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aef56-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="aef56-131">MOF</span><span class="sxs-lookup"><span data-stu-id="aef56-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef56-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aef56-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef56-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aef56-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef56-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef56-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="aef56-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aef56-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef56-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="aef56-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

