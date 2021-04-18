---
description: Ottiene l'identificazione digitale della chiave radice di archiviazione per un determinato modulo della parte pubblica della chiave radice di archiviazione TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Metodo Win32_Tpm:: GetSrkADThumbprint'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306370"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="d3fe6-103">\_Metodo Win32 TPM:: GetSrkADThumbprint</span><span class="sxs-lookup"><span data-stu-id="d3fe6-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="d3fe6-104">Ottiene l'identificazione digitale della chiave radice di archiviazione per un determinato modulo della parte pubblica della chiave radice di archiviazione TPM.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="d3fe6-105">L'identificazione personale viene utilizzata per indicizzare le chiavi radice di archiviazione nel server Active Directory se il backup Active Directory delle informazioni di autorizzazione del proprietario del TPM viene abilitato tramite Criteri di gruppo impostazione.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="d3fe6-106">A partire da Windows 10, versione 1607, l'autorizzazione del proprietario del TPM non viene mai sottoposta a backup in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="d3fe6-107">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3fe6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3fe6-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="d3fe6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3fe6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3fe6-110">*SrkPublicKeyModulus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3fe6-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3fe6-111">Modulo della parte pubblica della chiave radice di archiviazione TPM.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="d3fe6-112">È possibile ottenerlo anche usando il metodo [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) della classe [ \_ TPM Win32](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d3fe6-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe6-113">*SrkADThumbprint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3fe6-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3fe6-114">Restituisce una matrice di 20 byte contenente l'identificazione digitale della chiave radice di archiviazione per il modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3fe6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3fe6-115">Return value</span></span>

<span data-ttu-id="d3fe6-116">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d3fe6-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="d3fe6-117">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="d3fe6-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3fe6-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d3fe6-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3fe6-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d3fe6-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d3fe6-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d3fe6-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3fe6-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3fe6-122">Remarks</span></span>

<span data-ttu-id="d3fe6-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3fe6-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3fe6-124">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d3fe6-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d3fe6-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3fe6-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d3fe6-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3fe6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3fe6-127">Requirements</span></span>



| <span data-ttu-id="d3fe6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3fe6-128">Requirement</span></span> | <span data-ttu-id="d3fe6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d3fe6-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3fe6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3fe6-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d3fe6-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3fe6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3fe6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3fe6-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d3fe6-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d3fe6-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d3fe6-134">Namespace</span></span><br/>                | <span data-ttu-id="d3fe6-135">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="d3fe6-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="d3fe6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d3fe6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3fe6-137"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3fe6-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3fe6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d3fe6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3fe6-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d3fe6-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3fe6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3fe6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe6-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="d3fe6-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
