---
description: Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234038"
---
# <a name="msicertexe"></a><span data-ttu-id="daae4-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="daae4-103">Msicert.exe</span></span>

<span data-ttu-id="daae4-104">Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate.</span><span class="sxs-lookup"><span data-stu-id="daae4-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="daae4-105">Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna da installare dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="daae4-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="daae4-106">Per ulteriori informazioni, vedere [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="daae4-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="daae4-107">MsiCert.exe è un'utilità della riga di comando che può essere utilizzata per popolare la tabella [MsiDigitalSignature](msidigitalsignature-table.md) e la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md) con le informazioni sulla firma digitale di un file CAB esterno.</span><span class="sxs-lookup"><span data-stu-id="daae4-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="daae4-108">Il file CAB deve essere firmato digitalmente ed elencato nella [tabella dei supporti](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="daae4-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="daae4-109">MsiCert.exe usa le informazioni sul certificato del firmatario dall'armadio con firma digitale e crea e aggiunge le tabelle MsiDigitalSignature e MsiDigitalCertificate al database, se non esistono già.</span><span class="sxs-lookup"><span data-stu-id="daae4-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="daae4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="daae4-110">Syntax</span></span>

<span data-ttu-id="daae4-111">**msicert-d** *{database}* **-m** *{voce multimediale}* **-c** *{cabinet}* **\[ -h \]**</span><span class="sxs-lookup"><span data-stu-id="daae4-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="daae4-112">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="daae4-112">Command Line Options</span></span>

<span data-ttu-id="daae4-113">Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole e i delimitatori di barra possono essere utilizzati al posto di un trattino.</span><span class="sxs-lookup"><span data-stu-id="daae4-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="daae4-114">Opzione</span><span class="sxs-lookup"><span data-stu-id="daae4-114">Option</span></span> | <span data-ttu-id="daae4-115">Parametro</span><span class="sxs-lookup"><span data-stu-id="daae4-115">Parameter</span></span>        | <span data-ttu-id="daae4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="daae4-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daae4-117">-d</span><span class="sxs-lookup"><span data-stu-id="daae4-117">-d</span></span>     | <database> | <span data-ttu-id="daae4-118">Il database (file con estensione msi) in fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="daae4-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="daae4-119">-M</span><span class="sxs-lookup"><span data-stu-id="daae4-119">-m</span></span>     | <media Id> | <span data-ttu-id="daae4-120">Voce nel campo DiskID della [tabella dei supporti](media-table.md) nel record per il file CAB.</span><span class="sxs-lookup"><span data-stu-id="daae4-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="daae4-121">-c</span><span class="sxs-lookup"><span data-stu-id="daae4-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="daae4-122">Percorso del file CAB con firma digitale.</span><span class="sxs-lookup"><span data-stu-id="daae4-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="daae4-123">-H</span><span class="sxs-lookup"><span data-stu-id="daae4-123">-h</span></span>     |                  | <span data-ttu-id="daae4-124">Includere l'hash della firma digitale.</span><span class="sxs-lookup"><span data-stu-id="daae4-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="daae4-125">Questo indirizzo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="daae4-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="daae4-126">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="daae4-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="daae4-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daae4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daae4-128">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="daae4-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="daae4-129">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="daae4-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



