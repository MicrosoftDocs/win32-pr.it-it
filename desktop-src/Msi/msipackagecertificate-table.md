---
description: La tabella MsiPackageCertificate elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che rendono questo Multiple-Package installazione.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabella MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234036"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="7384d-103">Tabella MsiPackageCertificate</span><span class="sxs-lookup"><span data-stu-id="7384d-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="7384d-104">La tabella MsiPackageCertificate elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che rendono questa [installazione di più pacchetti](multiple-package-installations.md).</span><span class="sxs-lookup"><span data-stu-id="7384d-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="7384d-105">Usare questa tabella per creare un' [installazione di più pacchetti](multiple-package-installations.md) per un prodotto contenente più pacchetti Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7384d-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="7384d-106">Se il primo pacchetto è firmato digitalmente e contiene una tabella MsiPackageCertificate che specifica i certificati digitali per tutti i pacchetti rimanenti del prodotto, l'amministratore deve accettare solo la richiesta di [*controllo dell'account utente*](u-gly.md) (UAC) visualizzata per il primo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7384d-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="7384d-107">Dopo aver accettato la richiesta del controllo dell'account utente per il primo pacchetto, le funzioni definite dall'utente nella [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) possono quindi aggiungere i pacchetti rimanenti all'installazione di più pacchetti senza visualizzare una richiesta di controllo dell'account utente e richiedere una risposta dell'amministratore per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7384d-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="7384d-108">Se una o più funzioni nella [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) richiedono un pacchetto non firmato, viene visualizzato un altro messaggio di controllo dell'account utente che richiede l'interazione dell'amministratore per ogni pacchetto non firmato.</span><span class="sxs-lookup"><span data-stu-id="7384d-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="7384d-109">Se l'amministratore accetta questa richiesta di controllo dell'account utente, l'installazione di più pacchetti continua.</span><span class="sxs-lookup"><span data-stu-id="7384d-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="7384d-110">Una volta che un amministratore ha fornito le credenziali per un pacchetto, durante l'installazione di più pacchetti non verrà visualizzato alcun messaggio di richiesta del controllo dell'account utente per tale pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7384d-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="7384d-111">Se l'amministratore rifiuta una richiesta di controllo dell'account utente per un pacchetto, Windows Installer esegue il rollback dell'installazione di più pacchetti prima di eseguire il commit per installare i pacchetti appartenenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="7384d-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="7384d-112">**[Windows Installer 4,0 o versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="7384d-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="7384d-113">Questa tabella è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="7384d-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="7384d-114">La tabella MsiPackageCertificate include le colonne seguenti:</span><span class="sxs-lookup"><span data-stu-id="7384d-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="7384d-115">Colonna</span><span class="sxs-lookup"><span data-stu-id="7384d-115">Column</span></span>               | <span data-ttu-id="7384d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="7384d-116">Type</span></span>                         | <span data-ttu-id="7384d-117">Chiave</span><span class="sxs-lookup"><span data-stu-id="7384d-117">Key</span></span> | <span data-ttu-id="7384d-118">Nullable</span><span class="sxs-lookup"><span data-stu-id="7384d-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="7384d-119">PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="7384d-119">PackageCertificate</span></span>   | [<span data-ttu-id="7384d-120">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7384d-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="7384d-121">S</span><span class="sxs-lookup"><span data-stu-id="7384d-121">Y</span></span>   | <span data-ttu-id="7384d-122">N</span><span class="sxs-lookup"><span data-stu-id="7384d-122">N</span></span>        |
| <span data-ttu-id="7384d-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="7384d-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="7384d-124">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7384d-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="7384d-125">N</span><span class="sxs-lookup"><span data-stu-id="7384d-125">N</span></span>   | <span data-ttu-id="7384d-126">N</span><span class="sxs-lookup"><span data-stu-id="7384d-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7384d-127">Colonne</span><span class="sxs-lookup"><span data-stu-id="7384d-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7384d-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="7384d-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="7384d-129">Identificatore univoco per questa riga nella tabella MsiPackageCertificate.</span><span class="sxs-lookup"><span data-stu-id="7384d-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="7384d-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="7384d-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="7384d-131">Chiave esterna nella prima colonna della [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="7384d-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="7384d-132">La riga indicata nella tabella MsiDigitalCertificate contiene la rappresentazione binaria del certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="7384d-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="7384d-133">Convalida</span><span class="sxs-lookup"><span data-stu-id="7384d-133">Validation</span></span>

<dl>

[<span data-ttu-id="7384d-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="7384d-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="7384d-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="7384d-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="7384d-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7384d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7384d-137">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="7384d-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="7384d-138">Tabella MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="7384d-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



