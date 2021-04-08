---
title: Metodo IsLSRegisteredToSCP della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSRegisteredToSCP
- Metodo IsLSRegisteredToSCP Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSRegisteredToSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b203ff580c5ff8871d023c7f349626acdd693f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740186"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="4520b-106">Metodo IsLSRegisteredToSCP della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="4520b-106">IsLSRegisteredToSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="4520b-107">Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="4520b-107">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="4520b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4520b-108">Syntax</span></span>


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a><span data-ttu-id="4520b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4520b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4520b-110">*Registrato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4520b-110">*Registered* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4520b-111">Valore booleano che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="4520b-111">Boolean value that indicates whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4520b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4520b-112">Return value</span></span>

<span data-ttu-id="4520b-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4520b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4520b-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4520b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4520b-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4520b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4520b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4520b-116">Remarks</span></span>

<span data-ttu-id="4520b-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4520b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4520b-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4520b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4520b-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4520b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4520b-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4520b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4520b-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4520b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4520b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4520b-122">Requirements</span></span>



| <span data-ttu-id="4520b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4520b-123">Requirement</span></span> | <span data-ttu-id="4520b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4520b-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4520b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4520b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4520b-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4520b-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4520b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4520b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4520b-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4520b-128">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="4520b-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4520b-129">Namespace</span></span><br/>                | <span data-ttu-id="4520b-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4520b-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4520b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4520b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4520b-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4520b-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4520b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4520b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4520b-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4520b-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4520b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4520b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4520b-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="4520b-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

