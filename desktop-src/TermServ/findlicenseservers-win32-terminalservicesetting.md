---
title: Metodo FindLicenseServers della classe Win32_TerminalServiceSetting
description: Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FindLicenseServers
- Metodo FindLicenseServers Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964817"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="ecbab-106">Metodo FindLicenseServers della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="ecbab-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="ecbab-107">Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.</span><span class="sxs-lookup"><span data-stu-id="ecbab-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecbab-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="ecbab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecbab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbab-110">*LicenseServersList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ecbab-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbab-111">Elenco di oggetti [**\_ TSDiscoveredLicenseServer Win32**](win32-tsdiscoveredlicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbab-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="ecbab-112">Ogni oggetto nell'elenco di output ha il nome del server licenze Desktop remoto e il metodo di individuazione.</span><span class="sxs-lookup"><span data-stu-id="ecbab-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="ecbab-113">*Numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ecbab-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbab-114">Il numero totale di server licenze Desktop remoto individuati nell'elenco di output.</span><span class="sxs-lookup"><span data-stu-id="ecbab-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecbab-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecbab-115">Remarks</span></span>

<span data-ttu-id="ecbab-116">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ecbab-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ecbab-117">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="ecbab-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ecbab-118">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="ecbab-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ecbab-119">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ecbab-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ecbab-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ecbab-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ecbab-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ecbab-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ecbab-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ecbab-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ecbab-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ecbab-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbab-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecbab-124">Requirements</span></span>



| <span data-ttu-id="ecbab-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecbab-125">Requirement</span></span> | <span data-ttu-id="ecbab-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ecbab-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbab-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecbab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbab-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecbab-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecbab-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecbab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbab-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecbab-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecbab-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ecbab-131">Namespace</span></span><br/>                | <span data-ttu-id="ecbab-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ecbab-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ecbab-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ecbab-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecbab-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecbab-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecbab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ecbab-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecbab-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecbab-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbab-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecbab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbab-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ecbab-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

