---
title: Metodo SetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory
description: Imposta l'elenco configurato di indirizzi DNS idonei che possono essere utilizzati per il reindirizzamento.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetCurrentRedirectableAddresses
- Metodo SetCurrentRedirectableAddresses Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400779"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="cff74-106">Metodo SetCurrentRedirectableAddresses della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="cff74-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="cff74-107">Il metodo **SetCurrentRedirectableAddresses** imposta l'elenco configurato di indirizzi DNS idonei che possono essere usati per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="cff74-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff74-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cff74-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="cff74-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cff74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff74-110">*fTokenRedirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff74-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff74-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cff74-111">Type: **uint32**</span></span>

<span data-ttu-id="cff74-112">Flag che indica se deve essere utilizzato il reindirizzamento del token.</span><span class="sxs-lookup"><span data-stu-id="cff74-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cff74-113">*IPAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff74-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff74-114">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="cff74-114">Type: **string\[\]**</span></span>

<span data-ttu-id="cff74-115">Matrice di stringhe che rappresenta l'elenco di indirizzi IP idonei DNS che possono essere utilizzati per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="cff74-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff74-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cff74-116">Return value</span></span>

<span data-ttu-id="cff74-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cff74-117">Type: **uint32**</span></span>

<span data-ttu-id="cff74-118">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="cff74-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="cff74-119">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cff74-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cff74-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="cff74-120">Remarks</span></span>

<span data-ttu-id="cff74-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cff74-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cff74-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="cff74-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cff74-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="cff74-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cff74-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cff74-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cff74-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cff74-125">Requirements</span></span>



| <span data-ttu-id="cff74-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cff74-126">Requirement</span></span> | <span data-ttu-id="cff74-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cff74-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cff74-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cff74-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cff74-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cff74-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cff74-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cff74-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cff74-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cff74-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cff74-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cff74-132">Namespace</span></span><br/>                | <span data-ttu-id="cff74-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cff74-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cff74-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cff74-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cff74-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cff74-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cff74-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cff74-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff74-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cff74-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cff74-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cff74-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff74-139">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="cff74-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

