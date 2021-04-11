---
title: Metodo SetVirtualIPActive della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualIPActive
- Metodo SetVirtualIPActive Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964416"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="b86cb-106">Metodo SetVirtualIPActive della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="b86cb-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="b86cb-107">Imposta il valore della proprietà **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="b86cb-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b86cb-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="b86cb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b86cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86cb-110">*VirtualIPActive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86cb-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86cb-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b86cb-111">Type: **uint32**</span></span>

<span data-ttu-id="b86cb-112">Specifica se la virtualizzazione IP è attiva sul server.</span><span class="sxs-lookup"><span data-stu-id="b86cb-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="b86cb-113">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b86cb-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="b86cb-114">zero</span><span class="sxs-lookup"><span data-stu-id="b86cb-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="b86cb-115">La virtualizzazione IP non è attiva.</span><span class="sxs-lookup"><span data-stu-id="b86cb-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="b86cb-116">diverso da zero</span><span class="sxs-lookup"><span data-stu-id="b86cb-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="b86cb-117">La virtualizzazione IP è attiva.</span><span class="sxs-lookup"><span data-stu-id="b86cb-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86cb-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b86cb-118">Return value</span></span>

<span data-ttu-id="b86cb-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b86cb-119">Type: **uint32**</span></span>

<span data-ttu-id="b86cb-120">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b86cb-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b86cb-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b86cb-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b86cb-122">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b86cb-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86cb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b86cb-123">Requirements</span></span>



| <span data-ttu-id="b86cb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b86cb-124">Requirement</span></span> | <span data-ttu-id="b86cb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b86cb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b86cb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b86cb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b86cb-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b86cb-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b86cb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b86cb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b86cb-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b86cb-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b86cb-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b86cb-130">Namespace</span></span><br/>                | <span data-ttu-id="b86cb-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b86cb-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b86cb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b86cb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b86cb-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b86cb-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b86cb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b86cb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86cb-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86cb-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86cb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b86cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86cb-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="b86cb-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





