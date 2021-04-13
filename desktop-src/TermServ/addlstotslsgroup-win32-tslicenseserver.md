---
title: Metodo AddLStoTSLSGroup della classe Win32_TSLicenseServer
description: Aggiunge il server licenze Desktop remoto al gruppo server licenze di Connessione Desktop remoto broker (gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddLStoTSLSGroup
- Metodo AddLStoTSLSGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400464"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="9e65f-106">Metodo AddLStoTSLSGroup della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="9e65f-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9e65f-107">Aggiunge il server licenze Desktop remoto al gruppo server licenze di Connessione Desktop remoto broker (gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9e65f-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e65f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e65f-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="9e65f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e65f-109">Parameters</span></span>

<span data-ttu-id="9e65f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9e65f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e65f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e65f-111">Return value</span></span>

<span data-ttu-id="9e65f-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="9e65f-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9e65f-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9e65f-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9e65f-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9e65f-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e65f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e65f-115">Remarks</span></span>

<span data-ttu-id="9e65f-116">Per chiamare questo metodo, è necessario essere un membro del gruppo Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="9e65f-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="9e65f-117">Il server licenze deve essere membro del gruppo server licenze Desktop remoto se il server è configurato per l'utilizzo dell'ambito di individuazione dominio o foresta.</span><span class="sxs-lookup"><span data-stu-id="9e65f-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="9e65f-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9e65f-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9e65f-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9e65f-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9e65f-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9e65f-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9e65f-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9e65f-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e65f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e65f-122">Requirements</span></span>



| <span data-ttu-id="9e65f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e65f-123">Requirement</span></span> | <span data-ttu-id="9e65f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9e65f-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e65f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e65f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e65f-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9e65f-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9e65f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e65f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e65f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e65f-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9e65f-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e65f-129">Namespace</span></span><br/>                | <span data-ttu-id="9e65f-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9e65f-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9e65f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9e65f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e65f-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e65f-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e65f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e65f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e65f-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e65f-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e65f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e65f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e65f-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9e65f-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="9e65f-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9e65f-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

