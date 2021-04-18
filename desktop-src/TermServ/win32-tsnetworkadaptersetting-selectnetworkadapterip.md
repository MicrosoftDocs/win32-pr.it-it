---
title: Metodo SelectNetworkAdapterIP della classe Win32_TSNetworkAdapterSetting
description: Seleziona una scheda di rete in base all'indirizzo IP della scheda.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SelectNetworkAdapterIP
- Metodo SelectNetworkAdapterIP Servizi Desktop remoto, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, metodo SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301441"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="6ed85-106">Metodo SelectNetworkAdapterIP della \_ classe TSNetworkAdapterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="6ed85-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="6ed85-107">Seleziona una scheda di rete in base all'indirizzo IP della scheda.</span><span class="sxs-lookup"><span data-stu-id="6ed85-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed85-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ed85-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="6ed85-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ed85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed85-110">*NetworkAdapterIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ed85-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ed85-111">Indirizzo IP della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="6ed85-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed85-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ed85-112">Return value</span></span>

<span data-ttu-id="6ed85-113">Restituisce zero se l'indirizzo IP specificato è valido e restituisce un codice di errore WMI se l'indirizzo IP non è valido o non esiste.</span><span class="sxs-lookup"><span data-stu-id="6ed85-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="6ed85-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed85-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed85-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ed85-115">Remarks</span></span>

<span data-ttu-id="6ed85-116">È possibile recuperare l'indirizzo IP di una scheda di rete enumerando le proprietà della classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed85-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="6ed85-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6ed85-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6ed85-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6ed85-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6ed85-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed85-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6ed85-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6ed85-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed85-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ed85-121">Requirements</span></span>



| <span data-ttu-id="6ed85-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed85-122">Requirement</span></span> | <span data-ttu-id="6ed85-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6ed85-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed85-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ed85-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed85-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ed85-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ed85-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ed85-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed85-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ed85-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ed85-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ed85-128">Namespace</span></span><br/>                | <span data-ttu-id="6ed85-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6ed85-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6ed85-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6ed85-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ed85-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ed85-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ed85-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6ed85-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ed85-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ed85-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed85-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ed85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed85-135">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6ed85-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

