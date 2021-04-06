---
title: Metodo SetNetworkAdapterLanaID della classe Win32_TSNetworkAdapterSetting
description: Specifica il numero di scheda di rete locale (LANA) della scheda di rete da impostare.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetNetworkAdapterLanaID
- Metodo SetNetworkAdapterLanaID Servizi Desktop remoto, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, metodo SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743495"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="898d1-106">Metodo SetNetworkAdapterLanaID della \_ classe TSNetworkAdapterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="898d1-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="898d1-107">Il metodo **SetNetworkAdapterLanaID** specifica il numero di scheda di rete locale (lana) della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="898d1-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="898d1-108">Se l'ID di LANA specificato non è valido o non esiste, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="898d1-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="898d1-109">L'elenco di ID di LANA disponibile viene ottenuto enumerando la proprietà **DeviceIDList** nella classe [**\_ TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md) .</span><span class="sxs-lookup"><span data-stu-id="898d1-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="898d1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="898d1-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="898d1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="898d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="898d1-112">*NetworkAdapterLanaID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="898d1-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="898d1-113">Numero di LANA della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="898d1-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="898d1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="898d1-114">Return value</span></span>

<span data-ttu-id="898d1-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="898d1-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="898d1-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="898d1-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="898d1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="898d1-117">Remarks</span></span>

<span data-ttu-id="898d1-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="898d1-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="898d1-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="898d1-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="898d1-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="898d1-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="898d1-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="898d1-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="898d1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="898d1-122">Requirements</span></span>



| <span data-ttu-id="898d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="898d1-123">Requirement</span></span> | <span data-ttu-id="898d1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="898d1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="898d1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="898d1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="898d1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="898d1-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="898d1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="898d1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="898d1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="898d1-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="898d1-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="898d1-129">Namespace</span></span><br/>                | <span data-ttu-id="898d1-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="898d1-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="898d1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="898d1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="898d1-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="898d1-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="898d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="898d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="898d1-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="898d1-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="898d1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="898d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="898d1-136">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="898d1-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

