---
title: Metodo GetDomain della classe Win32_TerminalServiceSetting
description: Recupera il nome del dominio di cui è membro il server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- Metodo GetDomain Servizi Desktop remoto
- Metodo GetDomain Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, Metodo GetDomain
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963848"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0082a-106">Metodo GetDomain della classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="0082a-106">GetDomain method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0082a-107">Recupera il nome del dominio di cui è membro il server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="0082a-107">Retrieves the name of the domain that the Remote Desktop Session Host (RD Session Host) server is a member of.</span></span>

## <a name="syntax"></a><span data-ttu-id="0082a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0082a-108">Syntax</span></span>


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="0082a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0082a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0082a-110">*Dominio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0082a-110">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0082a-111">Nome di dominio del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0082a-111">The domain name of the RD Session Host server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0082a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0082a-112">Remarks</span></span>

<span data-ttu-id="0082a-113">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0082a-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0082a-114">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="0082a-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0082a-115">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="0082a-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="0082a-116">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0082a-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0082a-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0082a-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0082a-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0082a-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0082a-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0082a-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0082a-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0082a-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0082a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0082a-121">Requirements</span></span>



| <span data-ttu-id="0082a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0082a-122">Requirement</span></span> | <span data-ttu-id="0082a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0082a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0082a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0082a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0082a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0082a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0082a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0082a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0082a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0082a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0082a-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0082a-128">Namespace</span></span><br/>                | <span data-ttu-id="0082a-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0082a-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0082a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0082a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0082a-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0082a-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0082a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0082a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0082a-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0082a-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0082a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0082a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0082a-135">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0082a-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

