---
description: Crea un volume di BitLocker con il tipo di file system specificato del volume di individuazione.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Metodo PrepareVolume della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128750"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b8a50-103">Metodo PrepareVolume della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b8a50-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b8a50-104">Il metodo **PrepareVolume** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) crea un volume di BitLocker con il tipo di file system specificato del volume di individuazione.</span><span class="sxs-lookup"><span data-stu-id="b8a50-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="b8a50-105">Questo metodo deve essere chiamato prima che il volume possa essere protetto con uno qualsiasi dei metodi \**ProtectKeyWith \** _.</span><span class="sxs-lookup"><span data-stu-id="b8a50-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a50-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8a50-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="b8a50-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8a50-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a50-108">_DiscoveryVolumeType \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a50-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a50-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="b8a50-109">Type: **string**</span></span>

<span data-ttu-id="b8a50-110">Stringa che specifica il tipo di volume di individuazione.</span><span class="sxs-lookup"><span data-stu-id="b8a50-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="b8a50-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a50-111">Value</span></span>               | <span data-ttu-id="b8a50-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b8a50-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="b8a50-113">**&lt;nessuno&gt;**</span><span class="sxs-lookup"><span data-stu-id="b8a50-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="b8a50-114">Nessun volume di individuazione.</span><span class="sxs-lookup"><span data-stu-id="b8a50-114">No discovery volume.</span></span> <span data-ttu-id="b8a50-115">Questo valore consente di creare un volume nativo di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8a50-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="b8a50-116">**&lt;predefinita&gt;**</span><span class="sxs-lookup"><span data-stu-id="b8a50-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="b8a50-117">Questo valore è il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8a50-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="b8a50-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="b8a50-118">**FAT32**</span></span>           | <span data-ttu-id="b8a50-119">Questo valore consente di creare un volume di individuazione FAT32.</span><span class="sxs-lookup"><span data-stu-id="b8a50-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="b8a50-120">*ForceEncryptionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a50-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a50-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8a50-121">Type: **uint32**</span></span>

<span data-ttu-id="b8a50-122">Integer che specifica il tipo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b8a50-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="b8a50-123">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8a50-123">This can be one of the following values.</span></span>

| <span data-ttu-id="b8a50-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a50-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="b8a50-125">Significato</span><span class="sxs-lookup"><span data-stu-id="b8a50-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="b8a50-126">Non <dt>**specificato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8a50-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="b8a50-127">Il tipo di crittografia non è specificato.</span><span class="sxs-lookup"><span data-stu-id="b8a50-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="b8a50-128"><dt>**Software**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b8a50-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="b8a50-129">Crittografia software.</span><span class="sxs-lookup"><span data-stu-id="b8a50-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="b8a50-130"><dt>**Hardware**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b8a50-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="b8a50-131">Crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="b8a50-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a50-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8a50-132">Return value</span></span>

<span data-ttu-id="b8a50-133">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8a50-133">Type: **uint32**</span></span>

<span data-ttu-id="b8a50-134">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b8a50-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="b8a50-135">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8a50-135">Return code/value</span></span>      | <span data-ttu-id="b8a50-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8a50-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="b8a50-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="b8a50-137">**S_OK**</span></span> <br/> <span data-ttu-id="b8a50-138">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="b8a50-138">0 (0x0)</span></span> | <span data-ttu-id="b8a50-139">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b8a50-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="b8a50-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8a50-140">Remarks</span></span>

<span data-ttu-id="b8a50-141">Se questo metodo non viene chiamato quando si Abilita un volume di BitLocker, equivale a chiamare questo metodo con il valore predefinito nel parametro *DiscoveryVolumeType* .</span><span class="sxs-lookup"><span data-stu-id="b8a50-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a50-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8a50-142">Requirements</span></span>

| <span data-ttu-id="b8a50-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a50-143">Requirement</span></span> | <span data-ttu-id="b8a50-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a50-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a50-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a50-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a50-146">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a50-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b8a50-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a50-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a50-148">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a50-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8a50-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8a50-149">Namespace</span></span><br/>                | <span data-ttu-id="b8a50-150">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b8a50-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b8a50-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b8a50-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8a50-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8a50-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="b8a50-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8a50-153">See also</span></span>

[<span data-ttu-id="b8a50-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b8a50-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
