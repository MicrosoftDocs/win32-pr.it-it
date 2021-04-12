---
title: Metodo IsTSinTSCGroup della classe Win32_TSLicenseServer
description: Recupera un valore che indica se un server Host sessione Desktop remoto (host sessione Desktop remoto) è un membro del gruppo locale computer Terminal Server nel server licenze Desktop remoto.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsTSinTSCGroup
- Metodo IsTSinTSCGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsTSinTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518831"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="801a1-106">Metodo IsTSinTSCGroup della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="801a1-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="801a1-107">Recupera un valore che indica se un server Host sessione Desktop remoto (host sessione Desktop remoto) è un membro del gruppo locale computer Terminal Server nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="801a1-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="801a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="801a1-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="801a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="801a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="801a1-110">*tsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="801a1-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a1-111">Nome del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="801a1-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="801a1-112">*Membro* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="801a1-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="801a1-113">Valore booleano che indica se il server Host sessione Desktop remoto è un membro del gruppo locale computer Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="801a1-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="801a1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="801a1-114">Return value</span></span>

<span data-ttu-id="801a1-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="801a1-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="801a1-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="801a1-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="801a1-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="801a1-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="801a1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="801a1-118">Remarks</span></span>

<span data-ttu-id="801a1-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="801a1-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="801a1-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="801a1-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="801a1-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="801a1-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="801a1-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="801a1-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="801a1-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="801a1-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="801a1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="801a1-124">Requirements</span></span>



| <span data-ttu-id="801a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="801a1-125">Requirement</span></span> | <span data-ttu-id="801a1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="801a1-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="801a1-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="801a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="801a1-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="801a1-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="801a1-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="801a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="801a1-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="801a1-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="801a1-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="801a1-131">Namespace</span></span><br/>                | <span data-ttu-id="801a1-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="801a1-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="801a1-133">MOF</span><span class="sxs-lookup"><span data-stu-id="801a1-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="801a1-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="801a1-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="801a1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="801a1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="801a1-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="801a1-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="801a1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="801a1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801a1-138">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="801a1-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

