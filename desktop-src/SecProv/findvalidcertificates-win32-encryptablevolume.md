---
description: Enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Metodo FindValidCertificates della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347256"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c890e-103">Metodo FindValidCertificates della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="c890e-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c890e-104">Il metodo **FindValidCertificates** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali.</span><span class="sxs-lookup"><span data-stu-id="c890e-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="c890e-105">L'elenco restituito contiene solo certificati con un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) valido.</span><span class="sxs-lookup"><span data-stu-id="c890e-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="c890e-106">L'OID può essere il valore predefinito oppure può essere specificato nella Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c890e-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="c890e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c890e-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="c890e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c890e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c890e-109">*CertificateThumbprint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c890e-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c890e-110">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c890e-110">Type: **string\[\]**</span></span>

<span data-ttu-id="c890e-111">Matrice di stringhe che contiene l'elenco di certificati validi.</span><span class="sxs-lookup"><span data-stu-id="c890e-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c890e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c890e-112">Return value</span></span>

<span data-ttu-id="c890e-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c890e-113">Type: **uint32**</span></span>

<span data-ttu-id="c890e-114">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c890e-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c890e-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c890e-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="c890e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c890e-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c890e-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c890e-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="c890e-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c890e-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="c890e-119"><dt>**FVE \_ E \_ \_ \_ OID BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> non valido</span><span class="sxs-lookup"><span data-stu-id="c890e-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="c890e-120">L'OID di BitLocker disponibile non è valido.</span><span class="sxs-lookup"><span data-stu-id="c890e-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c890e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c890e-121">Requirements</span></span>



| <span data-ttu-id="c890e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c890e-122">Requirement</span></span> | <span data-ttu-id="c890e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c890e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c890e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c890e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c890e-125">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="c890e-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c890e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c890e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c890e-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c890e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c890e-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c890e-128">Namespace</span></span><br/>                | <span data-ttu-id="c890e-129">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c890e-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c890e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c890e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c890e-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c890e-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c890e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c890e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c890e-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c890e-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
