---
description: Consente di eseguire il backup dei dati di ripristino in Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Metodo BackupRecoveryInformationToActiveDirectory della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319336"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="89133-103">Metodo BackupRecoveryInformationToActiveDirectory della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="89133-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="89133-104">Il metodo **BackupRecoveryInformationToActiveDirectory** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) esegue il backup dei dati di ripristino in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="89133-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="89133-105">Questo metodo richiede che nel volume sia presente una protezione con password numerica.</span><span class="sxs-lookup"><span data-stu-id="89133-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="89133-106">Per consentire il backup delle informazioni di ripristino in Active Directory, è necessario configurare anche Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="89133-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="89133-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89133-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="89133-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89133-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89133-109">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89133-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89133-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="89133-110">Type: **string**</span></span>

<span data-ttu-id="89133-111">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="89133-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="89133-112">Questa protezione con chiave deve essere una protezione con password numerica.</span><span class="sxs-lookup"><span data-stu-id="89133-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89133-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89133-113">Return value</span></span>

<span data-ttu-id="89133-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89133-114">Type: **uint32**</span></span>

<span data-ttu-id="89133-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="89133-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="89133-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="89133-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="89133-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89133-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89133-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="89133-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="89133-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="89133-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="89133-120"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="89133-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="89133-121">Criteri di gruppo non consente di Active Directory l'archiviazione delle informazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89133-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="89133-122"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="89133-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="89133-123">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="89133-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="89133-124">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="89133-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="89133-125"><dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="89133-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="89133-126">La protezione con chiave specificata non è una protezione con chiave numerica.</span><span class="sxs-lookup"><span data-stu-id="89133-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="89133-127">È necessario immettere una protezione con password numerica.</span><span class="sxs-lookup"><span data-stu-id="89133-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="89133-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89133-128">Requirements</span></span>



| <span data-ttu-id="89133-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="89133-129">Requirement</span></span> | <span data-ttu-id="89133-130">Valore</span><span class="sxs-lookup"><span data-stu-id="89133-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89133-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89133-131">Minimum supported client</span></span><br/> | <span data-ttu-id="89133-132">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="89133-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89133-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89133-133">Minimum supported server</span></span><br/> | <span data-ttu-id="89133-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="89133-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="89133-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89133-135">Namespace</span></span><br/>                | <span data-ttu-id="89133-136">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="89133-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="89133-137">MOF</span><span class="sxs-lookup"><span data-stu-id="89133-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89133-138"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89133-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89133-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89133-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89133-140">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="89133-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




