---
description: Restituisce la chiave esterna da un file.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Metodo GetExternalKeyFromFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316113"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9bbdf-103">Metodo GetExternalKeyFromFile della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="9bbdf-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9bbdf-104">Il metodo **GetExternalKeyFromFile** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) restituisce la chiave esterna da un file creato da [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dato il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bbdf-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="9bbdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bbdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bbdf-107">*PathWithFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbdf-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-108">Type: **string**</span></span>

<span data-ttu-id="9bbdf-109">Stringa che specifica il percorso del file contenente una chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="9bbdf-110">*ExternalKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbdf-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="9bbdf-112">Matrice di byte che rappresenta la chiave esterna a 256 bit contenuta nel file che può essere utilizzata per sbloccare un volume.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bbdf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bbdf-113">Return value</span></span>

<span data-ttu-id="9bbdf-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-114">Type: **uint32**</span></span>

<span data-ttu-id="9bbdf-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9bbdf-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bbdf-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="9bbdf-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bbdf-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="9bbdf-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="9bbdf-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="9bbdf-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="9bbdf-121">Il file non contiene una chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="9bbdf-122"><dt>**Errore \_ FILE \_ non \_ trovato**</dt> <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="9bbdf-123">Impossibile trovare il file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9bbdf-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bbdf-124">Remarks</span></span>

<span data-ttu-id="9bbdf-125">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9bbdf-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9bbdf-126">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9bbdf-127">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9bbdf-128">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9bbdf-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbdf-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bbdf-129">Requirements</span></span>



| <span data-ttu-id="9bbdf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bbdf-130">Requirement</span></span> | <span data-ttu-id="9bbdf-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9bbdf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbdf-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bbdf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbdf-133">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9bbdf-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bbdf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbdf-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9bbdf-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9bbdf-136">Namespace</span></span><br/>                | <span data-ttu-id="9bbdf-137">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="9bbdf-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9bbdf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9bbdf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bbdf-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bbdf-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bbdf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bbdf-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
