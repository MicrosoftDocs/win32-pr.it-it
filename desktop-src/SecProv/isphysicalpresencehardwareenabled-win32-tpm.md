---
description: Il metodo IsPhysicalPresenceHardwareEnabled della \_ classe TPM Win32 indica se è possibile impostare la presenza fisica sulla piattaforma con un segnale hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Metodo IsPhysicalPresenceHardwareEnabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401645"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="88884-103">Metodo IsPhysicalPresenceHardwareEnabled della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="88884-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="88884-104">Il metodo **IsPhysicalPresenceHardwareEnabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se è possibile impostare la presenza fisica sulla piattaforma con un segnale hardware.</span><span class="sxs-lookup"><span data-stu-id="88884-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="88884-105">Questo valore viene configurato dal produttore della piattaforma in base alla progettazione della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="88884-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="88884-106">La documentazione del produttore della piattaforma può fornire ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="88884-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="88884-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88884-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="88884-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88884-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88884-109">*IsPhysicalPresenceHardwareEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88884-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88884-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="88884-110">Type: **boolean**</span></span>

<span data-ttu-id="88884-111">Se **true**, la presenza fisica sulla piattaforma può essere impostata con un segnale hardware.</span><span class="sxs-lookup"><span data-stu-id="88884-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88884-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88884-112">Return value</span></span>

<span data-ttu-id="88884-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88884-113">Type: **uint32**</span></span>

<span data-ttu-id="88884-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="88884-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="88884-115">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="88884-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="88884-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="88884-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="88884-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88884-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="88884-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="88884-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="88884-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="88884-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88884-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="88884-120">Remarks</span></span>

<span data-ttu-id="88884-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="88884-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="88884-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="88884-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="88884-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="88884-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="88884-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="88884-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88884-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88884-125">Requirements</span></span>



| <span data-ttu-id="88884-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="88884-126">Requirement</span></span> | <span data-ttu-id="88884-127">Valore</span><span class="sxs-lookup"><span data-stu-id="88884-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="88884-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88884-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88884-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88884-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="88884-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88884-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88884-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88884-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="88884-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88884-132">Namespace</span></span><br/>                | <span data-ttu-id="88884-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="88884-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="88884-134">MOF</span><span class="sxs-lookup"><span data-stu-id="88884-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88884-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88884-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="88884-136">DLL</span><span class="sxs-lookup"><span data-stu-id="88884-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88884-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="88884-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88884-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88884-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88884-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="88884-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
