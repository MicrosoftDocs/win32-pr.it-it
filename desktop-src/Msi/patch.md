---
description: Il programma di installazione imposta la proprietà PATCH su un elenco di patch da applicare chiamando MsiApplyPatch, MsiApplyMultiplePatches o l'opzione della riga di comando/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH (proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331055"
---
# <a name="patch-property"></a><span data-ttu-id="9291e-103">PATCH (proprietà)</span><span class="sxs-lookup"><span data-stu-id="9291e-103">PATCH property</span></span>

<span data-ttu-id="9291e-104">Il programma di installazione imposta la proprietà **patch** su un elenco di patch da applicare chiamando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) o l' [opzione della riga di comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="9291e-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="9291e-105">È inoltre possibile impostare la proprietà **patch** nella riga di comando durante l'installazione di un pacchetto tramite [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o l'opzione della riga di comando/i.</span><span class="sxs-lookup"><span data-stu-id="9291e-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="9291e-106">Il valore della proprietà **patch** è un elenco delle patch installate.</span><span class="sxs-lookup"><span data-stu-id="9291e-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="9291e-107">Ogni patch nell'elenco è rappresentata dal percorso completo del pacchetto della patch (file con estensione msp). I percorsi completi nell'elenco sono separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="9291e-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="9291e-108">**Windows Installer 2,0:** Non sono supportate più patch.</span><span class="sxs-lookup"><span data-stu-id="9291e-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="9291e-109">Per applicare più patch, è necessario Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="9291e-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="9291e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9291e-110">Remarks</span></span>

<span data-ttu-id="9291e-111">Se si crea un pacchetto di patch usando [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) è possibile specificare che un'azione o una finestra di dialogo viene eseguita solo quando viene applicata una particolare patch.</span><span class="sxs-lookup"><span data-stu-id="9291e-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="9291e-112">Quando si crea il pacchetto di patch, ad esempio test. msp, si crea un'immagine aggiornata del prodotto e un file delle proprietà di creazione patch.</span><span class="sxs-lookup"><span data-stu-id="9291e-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="9291e-113">Quando si crea il file delle proprietà di creazione patch, è possibile immettere un nome di proprietà, ad esempio PATCHFORTEST, nel campo MediaSrcPropName della tabella [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="9291e-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="9291e-114">Quando si creano le tabelle di sequenza dell'immagine aggiornata del prodotto, è possibile includere nella colonna condizione della tabella di sequenza un'istruzione condizionale per l'azione o la finestra di dialogo che si desidera rendere condizionale.</span><span class="sxs-lookup"><span data-stu-id="9291e-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="9291e-115">È ad esempio possibile utilizzare l'istruzione condizionale seguente per eseguire un'azione o una finestra di dialogo solo quando viene applicato test. msp.</span><span class="sxs-lookup"><span data-stu-id="9291e-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="9291e-116">PATCH E PATCHFORTEST E PATCH >< PATCHFORTEST</span><span class="sxs-lookup"><span data-stu-id="9291e-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="9291e-117">Poiché la proprietà **patch** può contenere più patch, utilizzare l'operatore Substring "><" per verificare la presenza di una patch particolare anziché dell'operatore Equals "=".</span><span class="sxs-lookup"><span data-stu-id="9291e-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="9291e-118">Per ulteriori informazioni sulle istruzioni condizionali, vedere la sezione [sintassi dell'istruzione condizionale](conditional-statement-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="9291e-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="9291e-119">Se si applica un elenco di patch che include test. msp, il programma di installazione imposta entrambe le proprietà.</span><span class="sxs-lookup"><span data-stu-id="9291e-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="9291e-120">Ad esempio, è possibile usare l' [opzione della riga di comando](command-line-options.md) /p per applicare un elenco di due patch.</span><span class="sxs-lookup"><span data-stu-id="9291e-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="9291e-121">**msiexec/qb/p \\ \\ Scratch \\ Scratch \\ xyz \\ patches \\ test. msp; \\ \\ Scratch \\ Scratch \\ xyz \\ bar. msp**</span><span class="sxs-lookup"><span data-stu-id="9291e-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="9291e-122">Il programma di installazione imposta le proprietà **patch** e PATCHFORTEST come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="9291e-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="9291e-123">PATCH = Scratch \\ \\ \\ Scratch \\ xyz \\ patches \\ test. msp; \\ \\ Scratch \\ Scratch \\ xyz \\ bar. msp</span><span class="sxs-lookup"><span data-stu-id="9291e-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="9291e-124">PATCHFORTEST = \\ \\ Scratch \\ Scratch \\ xyz \\ patches \\ test. msp</span><span class="sxs-lookup"><span data-stu-id="9291e-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="9291e-125">In questo caso, la condizione è TRUE e l'azione condizionale o la finestra di dialogo precedente può essere eseguita per ogni patch installata, test. msp e bar. msp.</span><span class="sxs-lookup"><span data-stu-id="9291e-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="9291e-126">Se test. msp non viene applicato, il programma di installazione non lo include nella proprietà **patch** e non imposta PATCHFORTEST.</span><span class="sxs-lookup"><span data-stu-id="9291e-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="9291e-127">In questo caso, la condizione precedente è FALSE e l'azione condizionale o la finestra di dialogo non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="9291e-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="9291e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9291e-128">Requirements</span></span>



| <span data-ttu-id="9291e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9291e-129">Requirement</span></span> | <span data-ttu-id="9291e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9291e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9291e-131">Versione</span><span class="sxs-lookup"><span data-stu-id="9291e-131">Version</span></span><br/> | <span data-ttu-id="9291e-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9291e-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9291e-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9291e-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9291e-134">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9291e-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9291e-135">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9291e-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9291e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9291e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9291e-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9291e-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9291e-138">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="9291e-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="9291e-139">Esempi di sintassi di istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="9291e-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




