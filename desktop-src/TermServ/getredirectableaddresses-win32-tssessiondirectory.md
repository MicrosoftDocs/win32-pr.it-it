---
title: Metodo GetRedirectableAddresses della classe Win32_TSSessionDirectory
description: Ottiene l'intero elenco di indirizzi DNS idonei.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetRedirectableAddresses
- Metodo GetRedirectableAddresses Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047882"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="d5ca6-106">Metodo GetRedirectableAddresses della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="d5ca6-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="d5ca6-107">Ottiene l'intero elenco di indirizzi DNS idonei.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ca6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5ca6-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="d5ca6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5ca6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ca6-110">*fTokenRedirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5ca6-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ca6-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-111">Type: **uint32**</span></span>

<span data-ttu-id="d5ca6-112">Flag che indica se deve essere utilizzato il reindirizzamento del token.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d5ca6-113">*IPAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5ca6-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ca6-114">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-114">Type: **string\[\]**</span></span>

<span data-ttu-id="d5ca6-115">Elenco completo degli indirizzi IP disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="d5ca6-116">*AdapterNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5ca6-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ca6-117">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-117">Type: **string\[\]**</span></span>

<span data-ttu-id="d5ca6-118">Elenco dei nomi delle schede di rete associati agli indirizzi disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="d5ca6-119">*NetConName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5ca6-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ca6-120">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-120">Type: **string\[\]**</span></span>

<span data-ttu-id="d5ca6-121">Elenco dei nomi di connessione di rete associati agli indirizzi disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ca6-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5ca6-122">Return value</span></span>

<span data-ttu-id="d5ca6-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-123">Type: **uint32**</span></span>

<span data-ttu-id="d5ca6-124">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d5ca6-125">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ca6-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ca6-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5ca6-126">Remarks</span></span>

<span data-ttu-id="d5ca6-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d5ca6-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d5ca6-128">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d5ca6-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d5ca6-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d5ca6-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d5ca6-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d5ca6-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ca6-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5ca6-131">Requirements</span></span>



| <span data-ttu-id="d5ca6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ca6-132">Requirement</span></span> | <span data-ttu-id="d5ca6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d5ca6-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ca6-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5ca6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ca6-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d5ca6-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d5ca6-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5ca6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ca6-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5ca6-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5ca6-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5ca6-138">Namespace</span></span><br/>                | <span data-ttu-id="d5ca6-139">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d5ca6-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d5ca6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d5ca6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5ca6-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5ca6-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5ca6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d5ca6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5ca6-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5ca6-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ca6-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5ca6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ca6-145">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="d5ca6-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

