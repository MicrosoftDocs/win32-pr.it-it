---
title: Metodo SetTSRedirectorMode della classe Win32_TSSessionDirectory
description: Imposta il valore per indicare se il server fungerà da redirector Servizi Desktop remoto.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetTSRedirectorMode
- Metodo SetTSRedirectorMode Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874445"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="24b84-106">Metodo SetTSRedirectorMode della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="24b84-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="24b84-107">Imposta il valore per indicare se il server fungerà da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="24b84-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b84-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24b84-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="24b84-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="24b84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b84-110">*TSRedirValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24b84-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24b84-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24b84-111">Type: **uint32**</span></span>

<span data-ttu-id="24b84-112">Consente di specificare se il server fungerà da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="24b84-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="24b84-113">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="24b84-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="24b84-114">0</span><span class="sxs-lookup"><span data-stu-id="24b84-114">0</span></span>
</dt> <dd>

<span data-ttu-id="24b84-115">Il server fungerà da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="24b84-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="24b84-116">1</span><span class="sxs-lookup"><span data-stu-id="24b84-116">1</span></span>
</dt> <dd>

<span data-ttu-id="24b84-117">Il server non fungerà da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="24b84-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b84-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24b84-118">Return value</span></span>

<span data-ttu-id="24b84-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24b84-119">Type: **uint32**</span></span>

<span data-ttu-id="24b84-120">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="24b84-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="24b84-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="24b84-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="24b84-122">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="24b84-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b84-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="24b84-123">Remarks</span></span>

<span data-ttu-id="24b84-124">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="24b84-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24b84-125">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="24b84-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24b84-126">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="24b84-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24b84-127">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="24b84-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24b84-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b84-128">Requirements</span></span>



| <span data-ttu-id="24b84-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b84-129">Requirement</span></span> | <span data-ttu-id="24b84-130">Valore</span><span class="sxs-lookup"><span data-stu-id="24b84-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24b84-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b84-131">Minimum supported client</span></span><br/> | <span data-ttu-id="24b84-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24b84-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24b84-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b84-133">Minimum supported server</span></span><br/> | <span data-ttu-id="24b84-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24b84-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="24b84-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="24b84-135">End of client support</span></span><br/>    | <span data-ttu-id="24b84-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24b84-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24b84-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="24b84-137">End of server support</span></span><br/>    | <span data-ttu-id="24b84-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24b84-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="24b84-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="24b84-139">Namespace</span></span><br/>                | <span data-ttu-id="24b84-140">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="24b84-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24b84-141">MOF</span><span class="sxs-lookup"><span data-stu-id="24b84-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24b84-142"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24b84-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="24b84-143">DLL</span><span class="sxs-lookup"><span data-stu-id="24b84-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b84-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b84-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b84-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24b84-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b84-146">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="24b84-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

