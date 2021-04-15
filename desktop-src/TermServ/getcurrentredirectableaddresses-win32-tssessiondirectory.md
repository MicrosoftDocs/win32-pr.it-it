---
title: Metodo GetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory
description: Ottiene l'elenco attualmente configurato degli indirizzi idonei DNS che possono essere usati per il reindirizzamento.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetCurrentRedirectableAddresses
- Metodo GetCurrentRedirectableAddresses Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo GetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478893"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="5bc71-106">Metodo GetCurrentRedirectableAddresses della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="5bc71-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="5bc71-107">Ottiene l'elenco attualmente configurato degli indirizzi idonei DNS che possono essere usati per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="5bc71-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc71-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bc71-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="5bc71-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bc71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc71-110">*fTokenRedirection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bc71-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc71-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc71-111">Type: **uint32**</span></span>

<span data-ttu-id="5bc71-112">Flag che indica se deve essere utilizzato il reindirizzamento del token.</span><span class="sxs-lookup"><span data-stu-id="5bc71-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="5bc71-113">*IPAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bc71-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc71-114">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5bc71-114">Type: **string\[\]**</span></span>

<span data-ttu-id="5bc71-115">Una matrice degli indirizzi IP idonei DNS attualmente configurati che possono essere usati per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="5bc71-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc71-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bc71-116">Return value</span></span>

<span data-ttu-id="5bc71-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc71-117">Type: **uint32**</span></span>

<span data-ttu-id="5bc71-118">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="5bc71-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="5bc71-119">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc71-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc71-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bc71-120">Remarks</span></span>

<span data-ttu-id="5bc71-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5bc71-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5bc71-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5bc71-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5bc71-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5bc71-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5bc71-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5bc71-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc71-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bc71-125">Requirements</span></span>



| <span data-ttu-id="5bc71-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc71-126">Requirement</span></span> | <span data-ttu-id="5bc71-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5bc71-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc71-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc71-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc71-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5bc71-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5bc71-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc71-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc71-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bc71-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5bc71-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5bc71-132">Namespace</span></span><br/>                | <span data-ttu-id="5bc71-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5bc71-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5bc71-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5bc71-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bc71-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bc71-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bc71-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc71-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc71-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bc71-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc71-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bc71-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc71-139">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="5bc71-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

