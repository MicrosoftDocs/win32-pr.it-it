---
title: Metodo SetVirtualIPMode della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualIPMode
- Metodo SetVirtualIPMode Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301964"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="def9a-106">Metodo SetVirtualIPMode della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="def9a-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="def9a-107">Imposta il valore della proprietà **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="def9a-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="def9a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="def9a-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="def9a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="def9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def9a-110">*VirtualIPMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def9a-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def9a-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="def9a-111">Type: **uint32**</span></span>

<span data-ttu-id="def9a-112">Specifica la modalità di virtualizzazione IP utilizzata nel server.</span><span class="sxs-lookup"><span data-stu-id="def9a-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="def9a-113">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="def9a-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="def9a-114">0</span><span class="sxs-lookup"><span data-stu-id="def9a-114">0</span></span>
</dt> <dd>

<span data-ttu-id="def9a-115">La modalità di virtualizzazione IP è per sessione.</span><span class="sxs-lookup"><span data-stu-id="def9a-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="def9a-116">1</span><span class="sxs-lookup"><span data-stu-id="def9a-116">1</span></span>
</dt> <dd>

<span data-ttu-id="def9a-117">La modalità di virtualizzazione IP è per utente.</span><span class="sxs-lookup"><span data-stu-id="def9a-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def9a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="def9a-118">Return value</span></span>

<span data-ttu-id="def9a-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="def9a-119">Type: **uint32**</span></span>

<span data-ttu-id="def9a-120">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="def9a-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="def9a-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="def9a-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="def9a-122">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="def9a-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="def9a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="def9a-123">Requirements</span></span>



| <span data-ttu-id="def9a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="def9a-124">Requirement</span></span> | <span data-ttu-id="def9a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="def9a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="def9a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="def9a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="def9a-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="def9a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="def9a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="def9a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="def9a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="def9a-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="def9a-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="def9a-130">Namespace</span></span><br/>                | <span data-ttu-id="def9a-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="def9a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="def9a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="def9a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="def9a-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="def9a-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="def9a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="def9a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def9a-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def9a-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def9a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="def9a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def9a-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="def9a-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





