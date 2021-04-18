---
description: Il metodo FileSignatureInfo dell'oggetto Installer accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresenta l'hash o il certificato codificato.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. FileSignatureInfo, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324625"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="3c108-103">Installer. FileSignatureInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="3c108-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="3c108-104">Il metodo **FileSignatureInfo** dell'oggetto [**Installer**](installer-object.md) accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresenta l'hash o il certificato codificato.</span><span class="sxs-lookup"><span data-stu-id="3c108-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="3c108-105">I valori possono quindi essere usati per popolare le tabelle [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3c108-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="3c108-106">Per ulteriori informazioni, vedere il [**tipo di dati SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="3c108-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c108-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c108-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="3c108-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c108-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="3c108-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="3c108-110">Percorso completo di un file con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3c108-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="3c108-111">Quando si popolano le tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* punta a un cabinet con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3c108-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="3c108-112">Quando si popolano le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *filePath* punta a una patch con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3c108-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="3c108-113">*Opzioni*</span><span class="sxs-lookup"><span data-stu-id="3c108-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="3c108-114">Flag speciali per i casi di errore.</span><span class="sxs-lookup"><span data-stu-id="3c108-114">Special error case flags.</span></span>



| <span data-ttu-id="3c108-115">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="3c108-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="3c108-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3c108-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="3c108-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c108-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3c108-118">Con le *Opzioni* impostate su MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** restituisce sempre un errore irreversibile per un hash non valido.</span><span class="sxs-lookup"><span data-stu-id="3c108-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="3c108-119">Se *options* non è impostato su MsiSignatureOptionInvalidHashFatal e *Format* è impostato su msiSignatureInfoCertificate, **FileSignatureInfo** non restituisce un errore per un hash non valido.</span><span class="sxs-lookup"><span data-stu-id="3c108-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c108-120">*Formato*</span><span class="sxs-lookup"><span data-stu-id="3c108-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="3c108-121">Informazioni sulla firma richieste.</span><span class="sxs-lookup"><span data-stu-id="3c108-121">The requested signature information.</span></span>



| <span data-ttu-id="3c108-122">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="3c108-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="3c108-123">Significato</span><span class="sxs-lookup"><span data-stu-id="3c108-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="3c108-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c108-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3c108-125">Restituisce un SAFEARRAY di byte che rappresenta il certificato codificato.</span><span class="sxs-lookup"><span data-stu-id="3c108-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="3c108-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c108-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="3c108-127">Restituisce un SAFEARRAY di byte che rappresenta l'hash.</span><span class="sxs-lookup"><span data-stu-id="3c108-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c108-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c108-128">Return value</span></span>

<span data-ttu-id="3c108-129">Se ha esito positivo, il metodo restituisce un [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) di byte che contiene il certificato hash o codificato.</span><span class="sxs-lookup"><span data-stu-id="3c108-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c108-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c108-130">Remarks</span></span>

<span data-ttu-id="3c108-131">Per creare un'installazione firmata completamente verificata tramite l'automazione, utilizzare il metodo **FileSignatureInfo** per popolare le tabelle [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature](msidigitalsignature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3c108-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="3c108-132">Per altre informazioni, vedere [creazione di un'installazione firmata completamente verificata usando l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="3c108-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c108-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c108-133">Requirements</span></span>



| <span data-ttu-id="3c108-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c108-134">Requirement</span></span> | <span data-ttu-id="3c108-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3c108-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c108-136">Versione</span><span class="sxs-lookup"><span data-stu-id="3c108-136">Version</span></span><br/> | <span data-ttu-id="3c108-137">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c108-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3c108-138">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c108-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3c108-139">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c108-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3c108-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3c108-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c108-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c108-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3c108-142">IID</span><span class="sxs-lookup"><span data-stu-id="3c108-142">IID</span></span><br/>     | <span data-ttu-id="3c108-143">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3c108-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3c108-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c108-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c108-145">Creazione di un'installazione firmata completamente verificata tramite l'automazione</span><span class="sxs-lookup"><span data-stu-id="3c108-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="3c108-146">Firme digitali e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3c108-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="3c108-147">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="3c108-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
