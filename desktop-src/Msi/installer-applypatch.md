---
description: Per ogni prodotto elencato dal pacchetto di patch come idoneo per la ricezione della patch, il Metodo ApplyPatch dell'oggetto del programma di installazione richiama un'installazione e imposta la proprietà PATCH sul percorso del pacchetto di patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. ApplyPatch, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328317"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="52f2f-103">Installer. ApplyPatch, metodo</span><span class="sxs-lookup"><span data-stu-id="52f2f-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="52f2f-104">Per ogni prodotto elencato dal pacchetto di patch come idoneo per la ricezione della patch, il metodo **applypatch** dell'oggetto del [**programma**](installer-object.md) di installazione richiama un'installazione e imposta la proprietà [**patch**](patch.md) sul percorso del pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52f2f-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="52f2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52f2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f2f-107">*PacchettoPatch*</span><span class="sxs-lookup"><span data-stu-id="52f2f-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="52f2f-108">Specifica il percorso del pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="52f2f-109">*InstallPackage*</span><span class="sxs-lookup"><span data-stu-id="52f2f-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="52f2f-110">Se *InstallType* è impostato su MsiInstallTypeNetworkImage, *InstallPackage* specifica il percorso del prodotto a cui applicare la patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="52f2f-111">Se *InstallType* è impostato su MsiInstallTypeDefault e *InstallPackage* è impostato su 0, il programma di installazione applica la patch a tutti i prodotti idonei elencati nel pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="52f2f-112">Se *InstallType* è msiInstallTypeSingleInstance, il programma di installazione applica la patch al prodotto specificato da *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="52f2f-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="52f2f-113">In questo caso, altri prodotti idonei elencati nel pacchetto di patch vengono ignorati e il parametro *InstallPackage* contiene la stringa con terminazione null che rappresenta il codice prodotto dell'istanza da applicare alla patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="52f2f-114">Per questo tipo di installazione è necessario che la versione del Windows Installer fornita con Windows Server 2003 o versione successiva o Windows Installer XP SP1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="52f2f-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="52f2f-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="52f2f-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="52f2f-116">Questo parametro specifica il tipo di installazione di cui applicare la patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="52f2f-117">Il parametro *InstallType* viene ignorato se *InstallPackage* viene omesso.</span><span class="sxs-lookup"><span data-stu-id="52f2f-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="52f2f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="52f2f-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="52f2f-119">Significato</span><span class="sxs-lookup"><span data-stu-id="52f2f-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="52f2f-120"><dt>**msiInstallTypeNetworkImage**</dt></span><span class="sxs-lookup"><span data-stu-id="52f2f-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="52f2f-121">Indica un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="52f2f-121">Indicates a administrative installation.</span></span> <span data-ttu-id="52f2f-122">In questo caso, *InstallPackage* deve essere impostato su un percorso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="52f2f-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="52f2f-123">Il valore 1 per msiInstallTypeNetworkImage specifica un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="52f2f-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="52f2f-124"><dt>**msiInstallTypeDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="52f2f-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="52f2f-125">Cerca nel sistema i prodotti da applicare alla patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-125">Searches system for products to patch.</span></span> <span data-ttu-id="52f2f-126">In questo caso, *InstallPackage* deve essere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="52f2f-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="52f2f-127"><dt>**msiInstallSingleInstance**</dt></span><span class="sxs-lookup"><span data-stu-id="52f2f-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="52f2f-128">Applicare patch al prodotto specificato da *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="52f2f-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="52f2f-129">*InstallPackage* è il codice prodotto dell'istanza da applicare alla patch.</span><span class="sxs-lookup"><span data-stu-id="52f2f-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="52f2f-130">Questo tipo di installazione richiede la versione Windows Installer fornita con Windows Server 2003 o versioni successive o Windows Installer XP SP1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="52f2f-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="52f2f-131">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="52f2f-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52f2f-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="52f2f-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="52f2f-133">Specifica le impostazioni delle proprietà impostate nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="52f2f-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="52f2f-134">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="52f2f-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f2f-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52f2f-135">Return value</span></span>

<span data-ttu-id="52f2f-136">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="52f2f-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f2f-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="52f2f-137">Remarks</span></span>

<span data-ttu-id="52f2f-138">Poiché il delimitatore di elenco per le trasformazioni, le origini e le patch è un punto e virgola, questo carattere non deve essere usato per i nomi file o i percorsi.</span><span class="sxs-lookup"><span data-stu-id="52f2f-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="52f2f-139">La proprietà [**REINSTALL**](reinstall.md) è obbligatoria quando si applica un [aggiornamento di piccole dimensioni](small-updates.md) o una patch di [aggiornamento secondaria](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="52f2f-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="52f2f-140">Senza questa proprietà, la patch è registrata nel sistema, ma non può aggiornare i file.</span><span class="sxs-lookup"><span data-stu-id="52f2f-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="52f2f-141">**Windows Installer 2,0:** È necessario impostare la proprietà [**REINSTALL**](reinstall.md) nella riga di comando quando si applica una patch di aggiornamento [piccola](small-updates.md) o [secondaria](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="52f2f-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="52f2f-142">Per le patch che non utilizzano un [tipo di azione personalizzato 51](custom-action-type-51.md) per impostare automaticamente le proprietà **REINSTALL** e [**REINSTALLMODE**](reinstallmode.md) , è necessario impostare in modo esplicito la proprietà **REINSTALL** con il parametro *CommandLine* .</span><span class="sxs-lookup"><span data-stu-id="52f2f-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="52f2f-143">Impostare la proprietà **REINSTALL** per elencare le funzionalità interessate dalla patch oppure utilizzare un'impostazione predefinita pratica "reinstall = all".</span><span class="sxs-lookup"><span data-stu-id="52f2f-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="52f2f-144">Il valore predefinito della proprietà **REINSTALLMODE** è "omus".</span><span class="sxs-lookup"><span data-stu-id="52f2f-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="52f2f-145">**Windows Installer 3,0 e versioni successive:** A partire da Windows Installer versione 3,0, la proprietà [**REINSTALL**](reinstall.md) viene configurata dal programma di installazione e non deve essere impostata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="52f2f-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f2f-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52f2f-146">Requirements</span></span>



| <span data-ttu-id="52f2f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f2f-147">Requirement</span></span> | <span data-ttu-id="52f2f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="52f2f-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f2f-149">Versione</span><span class="sxs-lookup"><span data-stu-id="52f2f-149">Version</span></span><br/> | <span data-ttu-id="52f2f-150">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52f2f-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52f2f-151">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52f2f-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52f2f-152">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52f2f-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="52f2f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="52f2f-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="52f2f-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52f2f-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="52f2f-155">IID</span><span class="sxs-lookup"><span data-stu-id="52f2f-155">IID</span></span><br/>     | <span data-ttu-id="52f2f-156">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="52f2f-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="52f2f-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52f2f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f2f-158">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="52f2f-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="52f2f-159">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="52f2f-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="52f2f-160">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="52f2f-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




