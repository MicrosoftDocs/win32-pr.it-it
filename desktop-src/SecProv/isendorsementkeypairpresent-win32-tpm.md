---
description: Il metodo IsEndorsementKeyPairPresent della \_ classe TPM Win32 indica se la coppia di chiavi di verifica dell'autenticità esiste nel dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Metodo IsEndorsementKeyPairPresent della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131987"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="9cd00-103">Metodo IsEndorsementKeyPairPresent della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="9cd00-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9cd00-104">Il metodo **IsEndorsementKeyPairPresent** della classe [**\_ TPM Win32**](win32-tpm.md) indica se la coppia di chiavi di verifica dell'autenticità esiste nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cd00-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="9cd00-105">La coppia di chiavi di verifica dell'autenticità è obbligatoria prima che il dispositivo possa essere proprietario.</span><span class="sxs-lookup"><span data-stu-id="9cd00-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="9cd00-106">Questa coppia di chiavi può essere creata dal metodo [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd00-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="9cd00-107">Il dispositivo deve essere abilitato e attivato affinché questo metodo abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9cd00-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="9cd00-108">Per abilitare e attivare un dispositivo senza proprietario, vedere il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd00-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd00-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cd00-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="9cd00-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cd00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd00-111">*IsEndorsementKeyPairPresent* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9cd00-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd00-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9cd00-112">Type: **boolean**</span></span>

<span data-ttu-id="9cd00-113">Se true, la coppia di chiavi di **Verifica dell'autenticità** esiste nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cd00-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd00-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cd00-114">Return value</span></span>

<span data-ttu-id="9cd00-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cd00-115">Type: **uint32**</span></span>

<span data-ttu-id="9cd00-116">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="9cd00-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9cd00-117">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="9cd00-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="9cd00-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cd00-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="9cd00-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd00-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9cd00-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9cd00-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9cd00-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="9cd00-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9cd00-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cd00-122">Remarks</span></span>

<span data-ttu-id="9cd00-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9cd00-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9cd00-124">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9cd00-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9cd00-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9cd00-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9cd00-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9cd00-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd00-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cd00-127">Requirements</span></span>



| <span data-ttu-id="9cd00-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd00-128">Requirement</span></span> | <span data-ttu-id="9cd00-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9cd00-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd00-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cd00-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd00-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cd00-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9cd00-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cd00-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd00-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cd00-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9cd00-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cd00-134">Namespace</span></span><br/>                | <span data-ttu-id="9cd00-135">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="9cd00-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9cd00-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9cd00-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cd00-137"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cd00-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cd00-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9cd00-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd00-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9cd00-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cd00-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cd00-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd00-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="9cd00-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9cd00-142">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="9cd00-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9cd00-143">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="9cd00-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
