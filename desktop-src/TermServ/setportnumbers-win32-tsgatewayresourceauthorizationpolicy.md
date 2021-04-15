---
title: Metodo SetPortNumbers della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta i numeri di porta consentiti per la connessione alla risorsa tramite Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPortNumbers
- Metodo SetPortNumbers Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477722"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="6bd39-106">Metodo SetPortNumbers della \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="6bd39-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="6bd39-107">Imposta i numeri di porta consentiti per la connessione alla risorsa tramite Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="6bd39-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd39-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bd39-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="6bd39-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bd39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd39-110">*PortNumbers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6bd39-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd39-111">Elenco di numeri di porta separati da punti e virgola consentiti per questo Desktop remoto Criteri di autorizzazione risorse (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="6bd39-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="6bd39-112">Per consentire qualsiasi numero di porta, impostare " \* ".</span><span class="sxs-lookup"><span data-stu-id="6bd39-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bd39-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bd39-113">Remarks</span></span>

<span data-ttu-id="6bd39-114">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6bd39-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6bd39-115">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6bd39-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6bd39-116">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6bd39-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6bd39-117">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6bd39-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd39-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bd39-118">Requirements</span></span>



| <span data-ttu-id="6bd39-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bd39-119">Requirement</span></span> | <span data-ttu-id="6bd39-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6bd39-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd39-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bd39-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd39-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6bd39-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6bd39-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bd39-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd39-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bd39-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6bd39-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6bd39-125">Namespace</span></span><br/>                | <span data-ttu-id="6bd39-126">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6bd39-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6bd39-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6bd39-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bd39-128"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bd39-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bd39-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd39-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bd39-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd39-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6bd39-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bd39-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd39-132">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="6bd39-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

