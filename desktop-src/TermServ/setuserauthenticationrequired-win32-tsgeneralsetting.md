---
title: Metodo SetUserAuthenticationRequired della classe Win32_TSGeneralSetting
description: Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserAuthenticationRequired
- Metodo SetUserAuthenticationRequired Servizi Desktop remoto, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, metodo SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341132"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="d0175-106">Metodo SetUserAuthenticationRequired della \_ classe TSGeneralSetting Win32</span><span class="sxs-lookup"><span data-stu-id="d0175-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="d0175-107">Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà **UserAuthenticationRequired** nella classe [**\_ TSGeneralSetting Win32**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d0175-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="d0175-108">Se **true**, ovvero abilitato, **UserAuthenticationRequired** richiede l'autenticazione dell'utente in fase di connessione per aumentare la protezione del server contro gli attacchi alla rete.</span><span class="sxs-lookup"><span data-stu-id="d0175-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="d0175-109">Solo i client Remote Desktop Protocol (RDP) che supportano la versione 6,0 o successiva di RDP sono in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="d0175-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="d0175-110">Per evitare le rotture per gli utenti remoti, è consigliabile distribuire i client RDP che supportano la versione del protocollo appropriata prima di abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="d0175-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0175-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0175-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="d0175-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0175-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0175-113">*UserAuthenticationRequired* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0175-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0175-114">Indica se è necessaria l'autenticazione utente.</span><span class="sxs-lookup"><span data-stu-id="d0175-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="d0175-115">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="d0175-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d0175-116">Disabilitare il requisito per cui l'utente deve essere autenticato</span><span class="sxs-lookup"><span data-stu-id="d0175-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="d0175-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d0175-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d0175-118">Abilita il requisito per cui l'utente deve essere autenticato.</span><span class="sxs-lookup"><span data-stu-id="d0175-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0175-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0175-119">Return value</span></span>

<span data-ttu-id="d0175-120">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d0175-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d0175-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d0175-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0175-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0175-122">Remarks</span></span>

<span data-ttu-id="d0175-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d0175-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d0175-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d0175-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d0175-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d0175-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d0175-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d0175-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0175-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0175-127">Requirements</span></span>



| <span data-ttu-id="d0175-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0175-128">Requirement</span></span> | <span data-ttu-id="d0175-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d0175-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0175-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0175-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d0175-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0175-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0175-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0175-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d0175-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0175-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0175-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d0175-134">Namespace</span></span><br/>                | <span data-ttu-id="d0175-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d0175-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d0175-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d0175-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0175-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0175-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0175-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d0175-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0175-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0175-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0175-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0175-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0175-141">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d0175-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

