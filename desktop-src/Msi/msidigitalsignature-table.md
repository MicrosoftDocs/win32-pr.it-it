---
description: La tabella MsiDigitalSignature contiene le informazioni sulla firma per ogni oggetto con firma digitale nel database di installazione.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabella MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310523"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="68a10-103">Tabella MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="68a10-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="68a10-104">La tabella MsiDigitalSignature contiene le informazioni sulla firma per ogni oggetto con firma digitale nel database di installazione.</span><span class="sxs-lookup"><span data-stu-id="68a10-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="68a10-105">Le tabelle MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) sono disponibili a partire dalla versione di Windows Installer 2,0.</span><span class="sxs-lookup"><span data-stu-id="68a10-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="68a10-106">Windows Installer versione può utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate.</span><span class="sxs-lookup"><span data-stu-id="68a10-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="68a10-107">Windows Installer 2,0 può verificare solo le firme digitali dei cabinet esterni e solo l'utilizzo delle tabelle MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="68a10-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="68a10-108">A partire da Windows Installer 3,0, il Windows Installer può verificare le firme digitali delle patch (file con estensione msp) usando le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="68a10-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="68a10-109">Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e l'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="68a10-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="68a10-110">La tabella MsiDigitalSignature include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="68a10-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="68a10-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="68a10-111">Column</span></span>               | <span data-ttu-id="68a10-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="68a10-112">Type</span></span>                         | <span data-ttu-id="68a10-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="68a10-113">Key</span></span> | <span data-ttu-id="68a10-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="68a10-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="68a10-115">Tabella</span><span class="sxs-lookup"><span data-stu-id="68a10-115">Table</span></span>                | [<span data-ttu-id="68a10-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="68a10-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="68a10-117">S</span><span class="sxs-lookup"><span data-stu-id="68a10-117">Y</span></span>   | <span data-ttu-id="68a10-118">N</span><span class="sxs-lookup"><span data-stu-id="68a10-118">N</span></span>        |
| <span data-ttu-id="68a10-119">SignObject</span><span class="sxs-lookup"><span data-stu-id="68a10-119">SignObject</span></span>           | [<span data-ttu-id="68a10-120">Text</span><span class="sxs-lookup"><span data-stu-id="68a10-120">Text</span></span>](text.md)             | <span data-ttu-id="68a10-121">S</span><span class="sxs-lookup"><span data-stu-id="68a10-121">Y</span></span>   | <span data-ttu-id="68a10-122">N</span><span class="sxs-lookup"><span data-stu-id="68a10-122">N</span></span>        |
| <span data-ttu-id="68a10-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="68a10-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="68a10-124">Identificatore</span><span class="sxs-lookup"><span data-stu-id="68a10-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="68a10-125">N</span><span class="sxs-lookup"><span data-stu-id="68a10-125">N</span></span>   | <span data-ttu-id="68a10-126">N</span><span class="sxs-lookup"><span data-stu-id="68a10-126">N</span></span>        |
| <span data-ttu-id="68a10-127">Hash</span><span class="sxs-lookup"><span data-stu-id="68a10-127">Hash</span></span>                 | [<span data-ttu-id="68a10-128">Binario</span><span class="sxs-lookup"><span data-stu-id="68a10-128">Binary</span></span>](binary.md)         | <span data-ttu-id="68a10-129">N</span><span class="sxs-lookup"><span data-stu-id="68a10-129">N</span></span>   | <span data-ttu-id="68a10-130">S</span><span class="sxs-lookup"><span data-stu-id="68a10-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="68a10-131">Colonne</span><span class="sxs-lookup"><span data-stu-id="68a10-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="68a10-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="68a10-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="68a10-133">Con la versione di Windows Installer 2,0, la voce in questo campo deve essere "media" per la [tabella dei supporti](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="68a10-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="68a10-134">Il programma di installazione verifica solo le firme digitali sulle voci multimediali del cabinet esterno.</span><span class="sxs-lookup"><span data-stu-id="68a10-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="68a10-135">Questa colonna e la colonna SignObject specificano insieme la risorsa con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="68a10-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="68a10-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span><span class="sxs-lookup"><span data-stu-id="68a10-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="68a10-137">Chiave esterna nella chiave primaria della tabella specificata dalla colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="68a10-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="68a10-138">Questa colonna e la colonna della tabella specificano insieme la risorsa con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="68a10-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="68a10-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="68a10-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="68a10-140">Chiave esterna nella [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="68a10-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="68a10-141">Identifica il certificato che deve esistere nel file affinché l'azione associata abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="68a10-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="68a10-142">È sempre necessario che la risorsa (o oggetto) corrisponda a questo certificato nella tabella MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="68a10-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="68a10-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span><span class="sxs-lookup"><span data-stu-id="68a10-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="68a10-144">In questo campo immettere l'hash di riferimento della risorsa (o oggetto) da verificare rispetto all'hash effettivo della risorsa (o oggetto) ottenuta in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="68a10-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="68a10-145">Se è necessario verificare solo il certificato, il campo hash può essere null.</span><span class="sxs-lookup"><span data-stu-id="68a10-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="68a10-146">Si noti che il formato dell'hash dipende dal tipo di risorsa (o oggetto) firmato.</span><span class="sxs-lookup"><span data-stu-id="68a10-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="68a10-147">La colonna hash contiene la rappresentazione binaria dell'hash.</span><span class="sxs-lookup"><span data-stu-id="68a10-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="68a10-148">Il contenuto effettivo è il membro **pbData** della struttura [**\_ \_ blob hash Crypt**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , che fa parte della struttura del **\_ BLOB CryptoAPI** .</span><span class="sxs-lookup"><span data-stu-id="68a10-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="68a10-149">Questa operazione può essere ottenuta chiamando [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) o [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span><span class="sxs-lookup"><span data-stu-id="68a10-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="68a10-150">Convalida</span><span class="sxs-lookup"><span data-stu-id="68a10-150">Validation</span></span>

<dl>

[<span data-ttu-id="68a10-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="68a10-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="68a10-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="68a10-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="68a10-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="68a10-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="68a10-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="68a10-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="68a10-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="68a10-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="68a10-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="68a10-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="68a10-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68a10-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68a10-158">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="68a10-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="68a10-159">Tabella MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="68a10-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="68a10-160">Firme digitali e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="68a10-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
