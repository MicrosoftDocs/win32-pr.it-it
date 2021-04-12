---
title: Metodo ExplicitLogon della classe Win32_TSLogonSetting
description: Il metodo ExplicitLogon imposta le credenziali da usare per l'autenticazione.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ExplicitLogon
- Metodo ExplicitLogon Servizi Desktop remoto, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Servizi Desktop remoto, metodo ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400774"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="4f298-106">Metodo ExplicitLogon della \_ classe TSLogonSetting Win32</span><span class="sxs-lookup"><span data-stu-id="4f298-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="4f298-107">Il metodo **ExplicitLogon** imposta le credenziali da usare per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="4f298-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f298-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f298-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="4f298-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f298-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f298-110">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f298-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f298-111">Credenziali di accesso del nome utente.</span><span class="sxs-lookup"><span data-stu-id="4f298-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="4f298-112">*Dominio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f298-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f298-113">Credenziali di accesso al dominio.</span><span class="sxs-lookup"><span data-stu-id="4f298-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="4f298-114">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4f298-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f298-115">Credenziali di accesso alla password.</span><span class="sxs-lookup"><span data-stu-id="4f298-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f298-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f298-116">Return value</span></span>

<span data-ttu-id="4f298-117">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="4f298-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4f298-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4f298-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4f298-119">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4f298-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f298-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f298-120">Remarks</span></span>

<span data-ttu-id="4f298-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f298-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f298-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4f298-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4f298-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4f298-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f298-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4f298-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f298-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f298-125">Requirements</span></span>



| <span data-ttu-id="4f298-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f298-126">Requirement</span></span> | <span data-ttu-id="4f298-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4f298-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f298-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f298-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f298-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f298-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f298-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f298-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f298-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f298-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f298-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f298-132">Namespace</span></span><br/>                | <span data-ttu-id="4f298-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4f298-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4f298-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4f298-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f298-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f298-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f298-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f298-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f298-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f298-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f298-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f298-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f298-139">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4f298-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

