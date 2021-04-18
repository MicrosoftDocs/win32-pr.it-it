---
title: Metodo SetVirtualizeLoopbackAddressesEnabled della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualizeLoopbackAddressesEnabled
- Metodo SetVirtualizeLoopbackAddressesEnabled Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301207"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="d99a0-106">Metodo SetVirtualizeLoopbackAddressesEnabled della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="d99a0-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="d99a0-107">Imposta il valore della proprietà **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="d99a0-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d99a0-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d99a0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d99a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99a0-110">*VirtualizeLoopbackAddressesEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99a0-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a0-111">Specifica se abilitare la virtualizzazione degli indirizzi di loopback.</span><span class="sxs-lookup"><span data-stu-id="d99a0-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="d99a0-112">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d99a0-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d99a0-113">0</span><span class="sxs-lookup"><span data-stu-id="d99a0-113">0</span></span>
</dt> <dd>

<span data-ttu-id="d99a0-114">Non abilitare la virtualizzazione degli indirizzi di loopback.</span><span class="sxs-lookup"><span data-stu-id="d99a0-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="d99a0-115">1</span><span class="sxs-lookup"><span data-stu-id="d99a0-115">1</span></span>
</dt> <dd>

<span data-ttu-id="d99a0-116">Abilitare la virtualizzazione degli indirizzi di loopback.</span><span class="sxs-lookup"><span data-stu-id="d99a0-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99a0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d99a0-117">Return value</span></span>

<span data-ttu-id="d99a0-118">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d99a0-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d99a0-119">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d99a0-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d99a0-120">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d99a0-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99a0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d99a0-121">Requirements</span></span>



| <span data-ttu-id="d99a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d99a0-122">Requirement</span></span> | <span data-ttu-id="d99a0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d99a0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d99a0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d99a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d99a0-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d99a0-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d99a0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d99a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d99a0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d99a0-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="d99a0-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d99a0-128">Namespace</span></span><br/>                | <span data-ttu-id="d99a0-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d99a0-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d99a0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d99a0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d99a0-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d99a0-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d99a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d99a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d99a0-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d99a0-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99a0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d99a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99a0-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="d99a0-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





