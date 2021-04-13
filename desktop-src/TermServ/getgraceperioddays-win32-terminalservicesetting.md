---
title: Metodo GetGracePeriodDays della classe Win32_TerminalServiceSetting
description: Recupera il numero di giorni rimanenti nel periodo di prova della licenza di Servizi Desktop remoto per un server di host sessione Desktop remoto (host sessione Desktop remoto). Un valore pari A zero indica che il periodo di tolleranza è scaduto.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetGracePeriodDays
- Metodo GetGracePeriodDays Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340473"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="95b44-107">Metodo GetGracePeriodDays della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="95b44-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="95b44-108">Recupera il numero di giorni rimanenti nel periodo di prova della licenza di Servizi Desktop remoto per un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="95b44-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="95b44-109">Un valore pari A zero indica che il periodo di tolleranza è scaduto.</span><span class="sxs-lookup"><span data-stu-id="95b44-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b44-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95b44-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="95b44-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="95b44-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b44-112">*DaysLeft* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95b44-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b44-113">Numero di giorni rimanenti nel periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="95b44-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95b44-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="95b44-114">Remarks</span></span>

<span data-ttu-id="95b44-115">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="95b44-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="95b44-116">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="95b44-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="95b44-117">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="95b44-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="95b44-118">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="95b44-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="95b44-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="95b44-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95b44-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="95b44-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="95b44-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="95b44-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95b44-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="95b44-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="95b44-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95b44-123">Requirements</span></span>



| <span data-ttu-id="95b44-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b44-124">Requirement</span></span> | <span data-ttu-id="95b44-125">Valore</span><span class="sxs-lookup"><span data-stu-id="95b44-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95b44-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95b44-126">Minimum supported client</span></span><br/> | <span data-ttu-id="95b44-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95b44-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95b44-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95b44-128">Minimum supported server</span></span><br/> | <span data-ttu-id="95b44-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95b44-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95b44-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95b44-130">Namespace</span></span><br/>                | <span data-ttu-id="95b44-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="95b44-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="95b44-132">MOF</span><span class="sxs-lookup"><span data-stu-id="95b44-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95b44-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95b44-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="95b44-134">DLL</span><span class="sxs-lookup"><span data-stu-id="95b44-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b44-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b44-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b44-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95b44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b44-137">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="95b44-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

