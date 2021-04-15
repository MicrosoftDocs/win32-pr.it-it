---
title: Metodo ConvertLicenses della classe Win32_TSLicenseKeyPack
description: Converte le licenze nel Key Pack corrente.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ConvertLicenses
- Metodo ConvertLicenses Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400335"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="81680-106">Metodo ConvertLicenses della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="81680-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="81680-107">Converte le licenze nel Key Pack corrente.</span><span class="sxs-lookup"><span data-stu-id="81680-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="81680-108">Se la licenza è una licenza per utente, viene convertita in una licenza per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81680-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="81680-109">Se la licenza è una licenza per ogni dispositivo, viene convertita in una licenza per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="81680-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="81680-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81680-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="81680-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="81680-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81680-112">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="81680-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81680-113">Numero di licenze da convertire.</span><span class="sxs-lookup"><span data-stu-id="81680-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="81680-114">*KeypackID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="81680-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81680-115">Identificatore del Key Pack risultante.</span><span class="sxs-lookup"><span data-stu-id="81680-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81680-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81680-116">Return value</span></span>

<span data-ttu-id="81680-117">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="81680-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="81680-118">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="81680-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="81680-119">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81680-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81680-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81680-120">Requirements</span></span>



| <span data-ttu-id="81680-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="81680-121">Requirement</span></span> | <span data-ttu-id="81680-122">Valore</span><span class="sxs-lookup"><span data-stu-id="81680-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81680-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81680-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81680-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="81680-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="81680-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81680-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81680-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81680-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="81680-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81680-127">Namespace</span></span><br/>                | <span data-ttu-id="81680-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="81680-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="81680-129">MOF</span><span class="sxs-lookup"><span data-stu-id="81680-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81680-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81680-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="81680-131">DLL</span><span class="sxs-lookup"><span data-stu-id="81680-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81680-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81680-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81680-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81680-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81680-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="81680-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





