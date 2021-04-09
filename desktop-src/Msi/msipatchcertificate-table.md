---
description: Identifica i possibili certificati del firmatario utilizzati per la firma digitale delle patch.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabella MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050144"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="6cb94-103">Tabella MsiPatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6cb94-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="6cb94-104">La tabella MsiPatchCertificate identifica i possibili certificati del firmatario usati per la firma digitale delle patch.</span><span class="sxs-lookup"><span data-stu-id="6cb94-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="6cb94-105">La tabella MsiPatchCertificate contiene le informazioni necessarie per abilitare l'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6cb94-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="6cb94-106">La tabella MsiPatchCertificate include le colonne seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cb94-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="6cb94-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="6cb94-107">Column</span></span>               | <span data-ttu-id="6cb94-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cb94-108">Type</span></span>                         | <span data-ttu-id="6cb94-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="6cb94-109">Key</span></span> | <span data-ttu-id="6cb94-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="6cb94-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="6cb94-111">PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6cb94-111">PatchCertificate</span></span>     | [<span data-ttu-id="6cb94-112">Identificatore</span><span class="sxs-lookup"><span data-stu-id="6cb94-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="6cb94-113">S</span><span class="sxs-lookup"><span data-stu-id="6cb94-113">Y</span></span>   | <span data-ttu-id="6cb94-114">N</span><span class="sxs-lookup"><span data-stu-id="6cb94-114">N</span></span>        |
| <span data-ttu-id="6cb94-115">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="6cb94-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="6cb94-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="6cb94-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="6cb94-117">N</span><span class="sxs-lookup"><span data-stu-id="6cb94-117">N</span></span>   | <span data-ttu-id="6cb94-118">N</span><span class="sxs-lookup"><span data-stu-id="6cb94-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6cb94-119">Colonne</span><span class="sxs-lookup"><span data-stu-id="6cb94-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6cb94-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6cb94-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="6cb94-121">Identificatore univoco per questa riga nella tabella MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="6cb94-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="6cb94-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="6cb94-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="6cb94-123">Chiave esterna nella prima colonna della [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="6cb94-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="6cb94-124">La riga indicata nella tabella MsiDigitalCertificate contiene la rappresentazione binaria del certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="6cb94-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cb94-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cb94-125">Remarks</span></span>

<span data-ttu-id="6cb94-126">Le patch vengono sempre valutate rispetto alla tabella MsiPatchCertificate corrente al momento dell'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="6cb94-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="6cb94-127">Una patch può modificare la tabella MsiPatchCertificate aggiungendo o rimuovendo le voci.</span><span class="sxs-lookup"><span data-stu-id="6cb94-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="6cb94-128">Questa operazione consente a una patch di modificare la valutazione delle patch future applicate successivamente nella sequenza di patch.</span><span class="sxs-lookup"><span data-stu-id="6cb94-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="6cb94-129">Nella tabella possono essere presenti più certificati e la patch deve corrispondere a almeno un certificato da applicare.</span><span class="sxs-lookup"><span data-stu-id="6cb94-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="6cb94-130">Convalida</span><span class="sxs-lookup"><span data-stu-id="6cb94-130">Validation</span></span>

<dl>

[<span data-ttu-id="6cb94-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="6cb94-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6cb94-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="6cb94-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6cb94-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="6cb94-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="6cb94-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="6cb94-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="6cb94-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cb94-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb94-136">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="6cb94-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="6cb94-137">Applicazione di patch al controllo dell'account utente (UAC)</span><span class="sxs-lookup"><span data-stu-id="6cb94-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="6cb94-138">**MSIDISABLELUAPATCHING**</span><span class="sxs-lookup"><span data-stu-id="6cb94-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="6cb94-139">Firme digitali e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6cb94-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="6cb94-140">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="6cb94-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



