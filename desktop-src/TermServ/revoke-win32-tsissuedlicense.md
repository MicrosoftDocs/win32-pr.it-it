---
title: Metodo Revoke della classe Win32_TSIssuedLicense
description: Revoca le licenze di accesso client per dispositivo Servizi Desktop remoto (RDS \ 160; Licenze CAL per dispositivo rappresentate dall' \_ oggetto Win32 TSIssuedLicense. Non si tratta di una funzione statica.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Metodo Revoke Servizi Desktop remoto
- Revoke (metodo) Servizi Desktop remoto, classe Win32_TSIssuedLicense
- Classe Win32_TSIssuedLicense Servizi Desktop remoto, Metodo Revoke
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743623"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="fd013-107">Metodo Revoke della \_ classe Win32 TSIssuedLicense</span><span class="sxs-lookup"><span data-stu-id="fd013-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="fd013-108">Revoca le licenze CAL per dispositivo Servizi Desktop remoto per ogni dispositivo rappresentate dall'oggetto [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="fd013-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="fd013-109">Non si tratta di una funzione statica.</span><span class="sxs-lookup"><span data-stu-id="fd013-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd013-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd013-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="fd013-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd013-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd013-112">*RevokableCals* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd013-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd013-113">Numero di licenze CAL Servizi Desktop remoto dello stesso tipo dell'oggetto corrente che può essere revocato.</span><span class="sxs-lookup"><span data-stu-id="fd013-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="fd013-114">*NextRevokeAllowedOn* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd013-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd013-115">Data in cui l'amministratore può provare a revocare le licenze.</span><span class="sxs-lookup"><span data-stu-id="fd013-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="fd013-116">Questo parametro contiene solo dati validi quando la chiamata al metodo **Revoke** non è riuscita perché è stato raggiunto il numero massimo di revoche.</span><span class="sxs-lookup"><span data-stu-id="fd013-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd013-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd013-117">Remarks</span></span>

<span data-ttu-id="fd013-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fd013-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fd013-119">È possibile revocare solo le licenze CAL per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd013-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="fd013-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fd013-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd013-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fd013-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd013-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fd013-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd013-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd013-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd013-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd013-124">Requirements</span></span>



| <span data-ttu-id="fd013-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd013-125">Requirement</span></span> | <span data-ttu-id="fd013-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fd013-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd013-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd013-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd013-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fd013-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fd013-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd013-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd013-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd013-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fd013-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd013-131">Namespace</span></span><br/>                | <span data-ttu-id="fd013-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fd013-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fd013-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fd013-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd013-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd013-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd013-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fd013-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd013-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd013-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd013-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd013-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd013-138">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="fd013-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

