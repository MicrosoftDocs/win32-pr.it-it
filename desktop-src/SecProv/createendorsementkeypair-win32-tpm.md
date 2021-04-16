---
description: Crea una coppia di chiavi di approvazione a 2048 bit nel TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Metodo CreateEndorsementKeyPair della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525692"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="6d4bc-103">Metodo CreateEndorsementKeyPair della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="6d4bc-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="6d4bc-104">Il metodo **CreateEndorsementKeyPair** della classe [**\_ TPM Win32**](win32-tpm.md) crea una coppia di chiavi di approvazione a 2048 bit nel TPM.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="6d4bc-105">Per eseguire correttamente il metodo [**TakeOwnership**](takeownership-win32-tpm.md) , è necessario che la coppia di chiavi di verifica dell'autenticità sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="6d4bc-106">È possibile utilizzare il metodo [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) per rilevare se la chiave di verifica dell'autenticità esiste già nel TPM.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d4bc-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="6d4bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d4bc-108">Parameters</span></span>

<span data-ttu-id="6d4bc-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d4bc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d4bc-110">Return value</span></span>

<span data-ttu-id="6d4bc-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d4bc-111">Type: **uint32**</span></span>

<span data-ttu-id="6d4bc-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="6d4bc-113">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="6d4bc-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d4bc-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6d4bc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d4bc-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="6d4bc-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6d4bc-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6d4bc-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="6d4bc-118"><dt> **TPM \_ E \_ disabilitato \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="6d4bc-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="6d4bc-119">Una coppia di chiavi di verifica dell'autenticità esiste già nel TPM.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d4bc-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d4bc-120">Remarks</span></span>

<span data-ttu-id="6d4bc-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6d4bc-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d4bc-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6d4bc-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d4bc-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6d4bc-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4bc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d4bc-125">Requirements</span></span>



| <span data-ttu-id="6d4bc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d4bc-126">Requirement</span></span> | <span data-ttu-id="6d4bc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6d4bc-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4bc-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d4bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4bc-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d4bc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d4bc-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d4bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4bc-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d4bc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6d4bc-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d4bc-132">Namespace</span></span><br/>                | <span data-ttu-id="6d4bc-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="6d4bc-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="6d4bc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6d4bc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d4bc-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d4bc-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d4bc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6d4bc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d4bc-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="6d4bc-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4bc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d4bc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4bc-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="6d4bc-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
