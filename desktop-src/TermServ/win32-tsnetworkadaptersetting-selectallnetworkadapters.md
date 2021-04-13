---
title: Metodo SelectAllNetworkAdapters della classe Win32_TSNetworkAdapterSetting
description: Il metodo SelectAllNetworkAdapters seleziona tutte le schede di rete.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SelectAllNetworkAdapters
- Metodo SelectAllNetworkAdapters Servizi Desktop remoto, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, metodo SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340863"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="8f9d3-106">Metodo SelectAllNetworkAdapters della \_ classe TSNetworkAdapterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="8f9d3-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="8f9d3-107">Il metodo **SelectAllNetworkAdapters** seleziona tutte le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="8f9d3-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9d3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f9d3-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="8f9d3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f9d3-109">Parameters</span></span>

<span data-ttu-id="8f9d3-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8f9d3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f9d3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f9d3-111">Return value</span></span>

<span data-ttu-id="8f9d3-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="8f9d3-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8f9d3-113">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d3-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9d3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f9d3-114">Remarks</span></span>

<span data-ttu-id="8f9d3-115">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8f9d3-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f9d3-116">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8f9d3-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f9d3-117">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8f9d3-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f9d3-118">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f9d3-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9d3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f9d3-119">Requirements</span></span>



| <span data-ttu-id="8f9d3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9d3-120">Requirement</span></span> | <span data-ttu-id="8f9d3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8f9d3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9d3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f9d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9d3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f9d3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f9d3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f9d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9d3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f9d3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f9d3-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f9d3-126">Namespace</span></span><br/>                | <span data-ttu-id="8f9d3-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f9d3-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f9d3-128">MOF</span><span class="sxs-lookup"><span data-stu-id="8f9d3-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f9d3-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d3-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f9d3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9d3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9d3-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d3-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9d3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f9d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9d3-133">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8f9d3-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

