---
description: Il metodo CreateAdvertiseScript dell'oggetto Installer genera uno script di annuncio.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Metodo Installer:: CreateAdvertiseScript'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333880"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="fc149-103">Metodo Installer:: CreateAdvertiseScript</span><span class="sxs-lookup"><span data-stu-id="fc149-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="fc149-104">Il metodo **CreateAdvertiseScript** dell'oggetto [**Installer**](installer-object.md) genera uno script di annuncio.</span><span class="sxs-lookup"><span data-stu-id="fc149-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc149-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc149-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="fc149-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc149-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="fc149-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-108">Percorso completo del pacchetto di Windows Installer (MSI) da annunciare.</span><span class="sxs-lookup"><span data-stu-id="fc149-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="fc149-109">*scriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="fc149-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-110">Percorso completo del file di script da creare con le informazioni annunciate.</span><span class="sxs-lookup"><span data-stu-id="fc149-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="fc149-111">*trasforma*</span><span class="sxs-lookup"><span data-stu-id="fc149-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-112">Elenco di trasformazioni da applicare al prodotto.</span><span class="sxs-lookup"><span data-stu-id="fc149-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="fc149-113">Le trasformazioni nell'elenco sono delimitate da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="fc149-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="fc149-114">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc149-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fc149-115">*language*</span><span class="sxs-lookup"><span data-stu-id="fc149-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-116">Lingua del pacchetto di installazione da usare.</span><span class="sxs-lookup"><span data-stu-id="fc149-116">The language of the installation package to use.</span></span> <span data-ttu-id="fc149-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc149-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fc149-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="fc149-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-119">Questo parametro specifica per quale piattaforma il programma di installazione deve creare lo script.</span><span class="sxs-lookup"><span data-stu-id="fc149-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="fc149-120">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc149-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fc149-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fc149-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="fc149-122">Significato</span><span class="sxs-lookup"><span data-stu-id="fc149-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="fc149-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="fc149-124">Crea uno script per la piattaforma corrente.</span><span class="sxs-lookup"><span data-stu-id="fc149-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="fc149-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="fc149-126">Crea uno script per la piattaforma x86.</span><span class="sxs-lookup"><span data-stu-id="fc149-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="fc149-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="fc149-128">Crea uno script per sistemi basati su Itanium.</span><span class="sxs-lookup"><span data-stu-id="fc149-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="fc149-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="fc149-130">Crea uno script per la piattaforma x64.</span><span class="sxs-lookup"><span data-stu-id="fc149-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="fc149-131">*options*</span><span class="sxs-lookup"><span data-stu-id="fc149-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="fc149-132">Opzioni dell'annuncio.</span><span class="sxs-lookup"><span data-stu-id="fc149-132">Advertisement options.</span></span> <span data-ttu-id="fc149-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc149-133">This parameter is optional.</span></span> <span data-ttu-id="fc149-134">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc149-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="fc149-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc149-135">This parameter is optional.</span></span>



| <span data-ttu-id="fc149-136">Valore</span><span class="sxs-lookup"><span data-stu-id="fc149-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="fc149-137">Significato</span><span class="sxs-lookup"><span data-stu-id="fc149-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="fc149-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="fc149-139">Annuncio standard</span><span class="sxs-lookup"><span data-stu-id="fc149-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="fc149-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="fc149-141">Annuncia una nuova istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="fc149-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="fc149-142">Richiede che la prima trasformazione nell'elenco di trasformazione del parametro *transforms* sia la trasformazione dell'istanza che modifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="fc149-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="fc149-143">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="fc149-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc149-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc149-144">Return value</span></span>

<span data-ttu-id="fc149-145">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fc149-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc149-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc149-146">Remarks</span></span>

<span data-ttu-id="fc149-147">Il metodo [**AdvertiseProduct**](installer-advertiseproduct.md) usa la funzione [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="fc149-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="fc149-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="fc149-148">Examples</span></span>

<span data-ttu-id="fc149-149">Nell'esempio seguente viene illustrato l'utilizzo del metodo **CreateAdvertiseScript** .</span><span class="sxs-lookup"><span data-stu-id="fc149-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="fc149-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc149-150">Requirements</span></span>



| <span data-ttu-id="fc149-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc149-151">Requirement</span></span> | <span data-ttu-id="fc149-152">Valore</span><span class="sxs-lookup"><span data-stu-id="fc149-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc149-153">Versione</span><span class="sxs-lookup"><span data-stu-id="fc149-153">Version</span></span><br/> | <span data-ttu-id="fc149-154">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc149-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc149-155">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc149-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc149-156">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc149-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="fc149-157">DLL</span><span class="sxs-lookup"><span data-stu-id="fc149-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc149-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="fc149-159">IID</span><span class="sxs-lookup"><span data-stu-id="fc149-159">IID</span></span><br/>     | <span data-ttu-id="fc149-160">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fc149-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="fc149-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc149-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc149-162">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="fc149-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="fc149-163">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="fc149-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




