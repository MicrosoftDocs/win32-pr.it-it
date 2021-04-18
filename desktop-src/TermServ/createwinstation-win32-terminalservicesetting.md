---
title: Metodo CreateWinstation della classe Win32_TerminalServiceSetting
description: Crea un nuovo stack del listener in base alla combinazione univoca di nome del listener e NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateWinstation
- Metodo CreateWinstation Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301129"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="7c4d8-106">Metodo CreateWinstation della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="7c4d8-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="7c4d8-107">Il metodo **CreateWinstation** crea un nuovo stack del listener in base alla combinazione univoca del nome del listener e della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c4d8-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="7c4d8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c4d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4d8-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c4d8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4d8-111">Nome del listener.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d8-112">*WinstaDriverName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c4d8-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4d8-113">Nome del driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d8-114">*LanaID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c4d8-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4d8-115">Numero di scheda di rete locale NetBIOS (LANA) per la scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4d8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c4d8-116">Return value</span></span>

<span data-ttu-id="7c4d8-117">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7c4d8-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c4d8-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4d8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c4d8-119">Remarks</span></span>

<span data-ttu-id="7c4d8-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c4d8-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7c4d8-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7c4d8-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7c4d8-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7c4d8-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7c4d8-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4d8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c4d8-124">Requirements</span></span>



| <span data-ttu-id="7c4d8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4d8-125">Requirement</span></span> | <span data-ttu-id="7c4d8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4d8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4d8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4d8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c4d8-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c4d8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4d8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c4d8-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c4d8-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c4d8-131">Namespace</span></span><br/>                | <span data-ttu-id="7c4d8-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7c4d8-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7c4d8-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7c4d8-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c4d8-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c4d8-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c4d8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7c4d8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c4d8-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c4d8-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4d8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c4d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4d8-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="7c4d8-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

