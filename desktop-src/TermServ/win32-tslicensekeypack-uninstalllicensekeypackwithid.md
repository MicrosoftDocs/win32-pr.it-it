---
title: Metodo UninstallLicenseKeyPackWithId della classe Win32_TSLicenseKeyPack
description: Disinstalla il Key Pack di Servizi Desktop remoto License con l'identificatore del Key Pack specificato.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UninstallLicenseKeyPackWithId
- Metodo UninstallLicenseKeyPackWithId Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475472"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="ead34-106">Metodo UninstallLicenseKeyPackWithId della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="ead34-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ead34-107">Disinstalla il Key Pack di Servizi Desktop remoto License con l'identificatore del Key Pack specificato.</span><span class="sxs-lookup"><span data-stu-id="ead34-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ead34-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="ead34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ead34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead34-110">*KeyPackId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ead34-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead34-111">Identificatore del Key Pack da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="ead34-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead34-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ead34-112">Return value</span></span>

<span data-ttu-id="ead34-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ead34-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ead34-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ead34-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ead34-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ead34-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ead34-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ead34-116">Requirements</span></span>



| <span data-ttu-id="ead34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead34-117">Requirement</span></span> | <span data-ttu-id="ead34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ead34-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead34-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ead34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ead34-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ead34-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ead34-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ead34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ead34-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ead34-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ead34-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ead34-123">Namespace</span></span><br/>                | <span data-ttu-id="ead34-124">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ead34-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ead34-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ead34-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ead34-126"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ead34-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ead34-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ead34-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead34-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead34-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead34-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ead34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead34-130">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="ead34-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





