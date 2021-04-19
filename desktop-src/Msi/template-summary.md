---
description: Per un pacchetto di installazione, la proprietà di riepilogo del modello indica le versioni della piattaforma e della lingua compatibili con il database di installazione.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Proprietà di riepilogo del modello
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326368"
---
# <a name="template-summary-property"></a><span data-ttu-id="2f7f7-103">Proprietà di riepilogo del modello</span><span class="sxs-lookup"><span data-stu-id="2f7f7-103">Template Summary property</span></span>

<span data-ttu-id="2f7f7-104">Per un pacchetto di installazione, la proprietà di **Riepilogo del modello** indica le versioni della piattaforma e della lingua compatibili con il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="2f7f7-105">La sintassi delle informazioni sulle proprietà di **Riepilogo dei modelli** per un database di installazione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="2f7f7-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="2f7f7-106">\[*Proprietà Platform* \] ; \[ *ID lingua* \] \[ ,*ID lingua* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="2f7f7-107">Gli esempi seguenti sono valori validi per la proprietà di **Riepilogo del modello** :</span><span class="sxs-lookup"><span data-stu-id="2f7f7-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="2f7f7-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-108">x64;1033</span></span>
-   <span data-ttu-id="2f7f7-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-109">Intel;1033</span></span>
-   <span data-ttu-id="2f7f7-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-110">Intel64;1033</span></span>
-   <span data-ttu-id="2f7f7-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-111">;1033</span></span>
-   <span data-ttu-id="2f7f7-112">Intel; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="2f7f7-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="2f7f7-113">Intel64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="2f7f7-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="2f7f7-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="2f7f7-114">Intel;0</span></span>
-   <span data-ttu-id="2f7f7-115">ARM; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="2f7f7-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="2f7f7-116">ARM; 0</span><span class="sxs-lookup"><span data-stu-id="2f7f7-116">Arm;0</span></span>
-   <span data-ttu-id="2f7f7-117">Arm64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="2f7f7-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="2f7f7-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="2f7f7-118">Arm64;0</span></span>

<span data-ttu-id="2f7f7-119">La proprietà di **Riepilogo del modello** di una trasformazione indica le versioni della piattaforma e della lingua compatibili con la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="2f7f7-120">In un file di trasformazione è possibile specificare solo una lingua.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="2f7f7-121">La piattaforma e la lingua specificate determinano se una trasformazione può essere applicata a un determinato database.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="2f7f7-122">La proprietà Platform e la proprietà Language possono essere lasciate vuote se nessuna restrizione di trasformazione si basa su di esse per convalidare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="2f7f7-123">La proprietà di **Riepilogo dei modelli** di un pacchetto di patch è un elenco delimitato da punti e virgola dei codici prodotto che possono accettare la patch.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="2f7f7-124">Se si usa [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) per generare il pacchetto di patch, questo elenco viene ottenuto dalla [tabella TargetImages](targetimages-table-patchwiz-dll-.md) del file di creazione della patch.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="2f7f7-125">Questa proprietà di riepilogo è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7f7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f7f7-126">Remarks</span></span>

<span data-ttu-id="2f7f7-127">Se la piattaforma corrente non corrisponde a una delle piattaforme specificate nella proprietà di **Riepilogo del modello** , il programma di installazione non elabora il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="2f7f7-128">Se la specifica della piattaforma non è presente nel valore della proprietà di **Riepilogo del modello** , il programma di installazione presuppone l'architettura Intel.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="2f7f7-129">Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione su una piattaforma Intel64 (Itanium), immettere Intel64 nella proprietà di **Riepilogo del modello** .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="2f7f7-130">Se si tratta di un pacchetto Windows Installer a 64 bit eseguito su una piattaforma x64, immettere x64 nella proprietà di **Riepilogo del modello** .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="2f7f7-131">Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione su una piattaforma Arm64, immettere Arm64 nella proprietà di **Riepilogo del modello** .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="2f7f7-132">Non è possibile contrassegnare un pacchetto di Windows Installer come supporto sia per Intel64 che per x64; ad esempio, il valore della proprietà di **Riepilogo del modello** di Intel64, x64 non è valido.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="2f7f7-133">Non è possibile contrassegnare un pacchetto di Windows Installer come supporto per piattaforme a 32 bit e a 64 bit. ad esempio, i valori delle proprietà di **Riepilogo dei modelli** come Intel, x64 o Intel, Intel64 non sono validi.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="2f7f7-134">Se si immette 0 (zero) nel campo ID lingua della proprietà **Riepilogo modello** o si lascia vuoto questo campo, viene indicato che il pacchetto è indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="2f7f7-135">Se si tratta di un pacchetto Windows Installer in esecuzione in Windows RT, immettere il valore ARM nella proprietà di **Riepilogo del modello** .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="2f7f7-136">I moduli merge sono gli unici pacchetti che possono avere più lingue.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="2f7f7-137">In un database del programma di installazione di origine è possibile specificare solo una lingua.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="2f7f7-138">Per ulteriori informazioni, vedere la pagina relativa ai [moduli merge con più lingue](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2f7f7-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="2f7f7-139">La piattaforma Alpha non è supportata da Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="2f7f7-140">**Windows Installer:** La sintassi seguente non è supportata:</span><span class="sxs-lookup"><span data-stu-id="2f7f7-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="2f7f7-141">\[*Proprietà Platform* \] \[ ,*Proprietà Platform* \] \[ \] ,... \[ *ID lingua* \] \[ ,*ID lingua* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="2f7f7-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="2f7f7-142">Gli esempi seguenti non sono valori validi per la proprietà di **Riepilogo dei modelli** :</span><span class="sxs-lookup"><span data-stu-id="2f7f7-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="2f7f7-143">Alfa, Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="2f7f7-144">Intel, Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="2f7f7-145">Alfa; 1033</span><span class="sxs-lookup"><span data-stu-id="2f7f7-145">Alpha;1033</span></span>
-   <span data-ttu-id="2f7f7-146">Alfa; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="2f7f7-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7f7-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f7f7-147">Requirements</span></span>



| <span data-ttu-id="2f7f7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7f7-148">Requirement</span></span> | <span data-ttu-id="2f7f7-149">Valore</span><span class="sxs-lookup"><span data-stu-id="2f7f7-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7f7-150">Versione</span><span class="sxs-lookup"><span data-stu-id="2f7f7-150">Version</span></span><br/> | <span data-ttu-id="2f7f7-151">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2f7f7-152">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2f7f7-153">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f7f7-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f7f7-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f7f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7f7-155">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="2f7f7-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




