---
title: Metodo UninstallLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Disinstalla un Key Pack per le licenze Servizi Desktop remoto.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UninstallLicenseKeyPack
- Metodo UninstallLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400272"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="7fb5b-106">Metodo UninstallLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="7fb5b-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="7fb5b-107">Disinstalla un Key Pack per le licenze Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb5b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fb5b-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="7fb5b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fb5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb5b-110">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fb5b-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-111">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="7fb5b-112">0</span><span class="sxs-lookup"><span data-stu-id="7fb5b-112">0</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-113">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7fb5b-114">1</span><span class="sxs-lookup"><span data-stu-id="7fb5b-114">1</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-115">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7fb5b-116">2</span><span class="sxs-lookup"><span data-stu-id="7fb5b-116">2</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fb5b-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7fb5b-118">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fb5b-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-119">Tipo di prodotto del Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="7fb5b-120">0</span><span class="sxs-lookup"><span data-stu-id="7fb5b-120">0</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-121">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="7fb5b-122">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="7fb5b-123">1</span><span class="sxs-lookup"><span data-stu-id="7fb5b-123">1</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-124">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="7fb5b-125">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="7fb5b-126">2</span><span class="sxs-lookup"><span data-stu-id="7fb5b-126">2</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-127">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7fb5b-128">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fb5b-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb5b-129">Numero di licenze da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb5b-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fb5b-130">Return value</span></span>

<span data-ttu-id="7fb5b-131">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7fb5b-132">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7fb5b-133">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7fb5b-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb5b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fb5b-134">Requirements</span></span>



| <span data-ttu-id="7fb5b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fb5b-135">Requirement</span></span> | <span data-ttu-id="7fb5b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7fb5b-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb5b-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fb5b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7fb5b-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7fb5b-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7fb5b-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fb5b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7fb5b-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fb5b-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7fb5b-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7fb5b-141">Namespace</span></span><br/>                | <span data-ttu-id="7fb5b-142">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7fb5b-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7fb5b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7fb5b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fb5b-144"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fb5b-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fb5b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7fb5b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fb5b-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fb5b-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb5b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fb5b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb5b-148">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="7fb5b-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





