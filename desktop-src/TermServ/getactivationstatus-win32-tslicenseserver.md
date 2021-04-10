---
title: Metodo GetActivationStatus della classe Win32_TSLicenseServer
description: Recupera lo stato di attivazione corrente del server licenze Desktop remoto.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetActivationStatus
- Metodo GetActivationStatus Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo GetActivationStatus
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f6209cd13c2372316e6a9606a3bc4fcd60fdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120210"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a5d84-106">Metodo GetActivationStatus della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="a5d84-106">GetActivationStatus method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a5d84-107">Recupera lo stato di attivazione corrente del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a5d84-107">Retrieves the current activation status of the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d84-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d84-108">Syntax</span></span>


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a5d84-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5d84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d84-110">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a5d84-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5d84-111">Lo stato di attivazione restituito può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="a5d84-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="a5d84-112">0</span><span class="sxs-lookup"><span data-stu-id="a5d84-112">0</span></span>
</dt> <dd>

<span data-ttu-id="a5d84-113">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="a5d84-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="a5d84-114">1</span><span class="sxs-lookup"><span data-stu-id="a5d84-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a5d84-115">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="a5d84-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="a5d84-116">2</span><span class="sxs-lookup"><span data-stu-id="a5d84-116">2</span></span>
</dt> <dd>

<span data-ttu-id="a5d84-117">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a5d84-117">An unknown error occurred.</span></span> <span data-ttu-id="a5d84-118">Non è noto se il server licenze Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="a5d84-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d84-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5d84-119">Return value</span></span>

<span data-ttu-id="a5d84-120">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a5d84-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a5d84-121">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a5d84-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a5d84-122">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a5d84-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d84-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5d84-123">Remarks</span></span>

<span data-ttu-id="a5d84-124">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="a5d84-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a5d84-125">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5d84-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5d84-126">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a5d84-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5d84-127">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a5d84-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5d84-128">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a5d84-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d84-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d84-129">Requirements</span></span>



| <span data-ttu-id="a5d84-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d84-130">Requirement</span></span> | <span data-ttu-id="a5d84-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d84-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d84-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d84-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d84-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a5d84-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a5d84-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d84-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d84-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5d84-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a5d84-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5d84-136">Namespace</span></span><br/>                | <span data-ttu-id="a5d84-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a5d84-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a5d84-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a5d84-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5d84-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5d84-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5d84-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d84-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d84-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5d84-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d84-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d84-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d84-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a5d84-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

