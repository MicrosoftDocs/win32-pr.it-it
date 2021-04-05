---
description: La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabella MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755415"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="55488-103">Tabella MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="55488-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="55488-104">La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="55488-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="55488-105">La chiave primaria viene utilizzata per condividere i certificati tra più oggetti con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="55488-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="55488-106">Un certificato digitale è una credenziale che fornisce un mezzo per verificare l'identità.</span><span class="sxs-lookup"><span data-stu-id="55488-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="55488-107">Per ulteriori informazioni, vedere la sezione relativa alla [crittografia](../seccrypto/cryptography-portal.md) del Software Development Kit (SDK [) di Microsoft](../seccrypto/digital-certificates.md) Windows.</span><span class="sxs-lookup"><span data-stu-id="55488-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="55488-108">Le tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate sono disponibili a partire dalla versione di Windows Installer 2,0.</span><span class="sxs-lookup"><span data-stu-id="55488-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="55488-109">Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate.</span><span class="sxs-lookup"><span data-stu-id="55488-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="55488-110">Windows Installer versione 2,0 è in grado di verificare solo le firme digitali dei cabinet esterni e solo l'utilizzo delle tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="55488-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="55488-111">A partire da Windows Installer versione 3,0, l'Windows Installer può verificare le firme digitali delle patch (file con estensione msp) usando le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="55488-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="55488-112">Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e l'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="55488-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="55488-113">La tabella MsiDigitalCertificate include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="55488-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="55488-114">Colonna</span><span class="sxs-lookup"><span data-stu-id="55488-114">Column</span></span>             | <span data-ttu-id="55488-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="55488-115">Type</span></span>                         | <span data-ttu-id="55488-116">Chiave</span><span class="sxs-lookup"><span data-stu-id="55488-116">Key</span></span> | <span data-ttu-id="55488-117">Nullable</span><span class="sxs-lookup"><span data-stu-id="55488-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="55488-118">DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="55488-118">DigitalCertificate</span></span> | [<span data-ttu-id="55488-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="55488-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="55488-120">S</span><span class="sxs-lookup"><span data-stu-id="55488-120">Y</span></span>   | <span data-ttu-id="55488-121">N</span><span class="sxs-lookup"><span data-stu-id="55488-121">N</span></span>        |
| <span data-ttu-id="55488-122">CertData</span><span class="sxs-lookup"><span data-stu-id="55488-122">CertData</span></span>           | [<span data-ttu-id="55488-123">Binario</span><span class="sxs-lookup"><span data-stu-id="55488-123">Binary</span></span>](binary.md)         | <span data-ttu-id="55488-124">N</span><span class="sxs-lookup"><span data-stu-id="55488-124">N</span></span>   | <span data-ttu-id="55488-125">N</span><span class="sxs-lookup"><span data-stu-id="55488-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="55488-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="55488-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="55488-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="55488-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="55488-128">Identifica il certificato di firma digitale.</span><span class="sxs-lookup"><span data-stu-id="55488-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="55488-129">Chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="55488-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="55488-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span><span class="sxs-lookup"><span data-stu-id="55488-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="55488-131">Rappresentazione binaria del certificato digitale.</span><span class="sxs-lookup"><span data-stu-id="55488-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="55488-132">La colonna CertData contiene la matrice di byte codificata di un contesto del certificato.</span><span class="sxs-lookup"><span data-stu-id="55488-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="55488-133">Si tratta del membro **pbCertEncoded** della struttura [**del \_ contesto del certificato**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="55488-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="55488-134">Il contesto del certificato può essere ottenuto chiamando [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un file con estensione cer.</span><span class="sxs-lookup"><span data-stu-id="55488-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="55488-135">Convalida</span><span class="sxs-lookup"><span data-stu-id="55488-135">Validation</span></span>

<dl>

[<span data-ttu-id="55488-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="55488-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="55488-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="55488-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="55488-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="55488-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="55488-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="55488-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="55488-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="55488-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="55488-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="55488-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="55488-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55488-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55488-143">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="55488-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="55488-144">Tabella MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="55488-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="55488-145">Firme digitali e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="55488-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
