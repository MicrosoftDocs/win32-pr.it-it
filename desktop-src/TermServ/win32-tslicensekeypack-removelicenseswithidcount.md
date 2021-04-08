---
title: Metodo RemoveLicensesWithIdCount della classe Win32_TSLicenseKeyPack
description: Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveLicensesWithIdCount
- Metodo RemoveLicensesWithIdCount Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047954"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c4067-106">Metodo RemoveLicensesWithIdCount della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="c4067-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c4067-107">Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.</span><span class="sxs-lookup"><span data-stu-id="c4067-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4067-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4067-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="c4067-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4067-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4067-110">*KeyPackId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4067-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4067-111">Identificatore del Key Pack che contiene le licenze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c4067-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="c4067-112">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4067-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4067-113">Numero di licenze da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="c4067-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4067-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4067-114">Return value</span></span>

<span data-ttu-id="c4067-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c4067-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c4067-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c4067-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c4067-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c4067-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4067-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4067-118">Requirements</span></span>



| <span data-ttu-id="c4067-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4067-119">Requirement</span></span> | <span data-ttu-id="c4067-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c4067-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4067-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4067-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4067-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c4067-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c4067-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4067-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4067-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4067-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c4067-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c4067-125">Namespace</span></span><br/>                | <span data-ttu-id="c4067-126">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c4067-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c4067-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c4067-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4067-128"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4067-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4067-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c4067-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4067-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4067-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4067-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4067-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4067-132">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="c4067-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





