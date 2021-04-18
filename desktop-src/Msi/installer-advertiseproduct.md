---
description: Il metodo AdvertiseProduct dell'oggetto Installer annuncia un pacchetto di installazione.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Metodo Installer:: AdvertiseProduct'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328324"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="022d1-103">Metodo Installer:: AdvertiseProduct</span><span class="sxs-lookup"><span data-stu-id="022d1-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="022d1-104">Il metodo **AdvertiseProduct** dell'oggetto [**Installer**](installer-object.md) annuncia un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="022d1-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="022d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="022d1-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="022d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="022d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="022d1-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="022d1-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="022d1-108">Percorso completo del pacchetto di Windows Installer (MSI) da annunciare.</span><span class="sxs-lookup"><span data-stu-id="022d1-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="022d1-109">*context*</span><span class="sxs-lookup"><span data-stu-id="022d1-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="022d1-110">Contesto dell'annuncio.</span><span class="sxs-lookup"><span data-stu-id="022d1-110">The context of the advertisement.</span></span> <span data-ttu-id="022d1-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="022d1-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="022d1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="022d1-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="022d1-113">Significato</span><span class="sxs-lookup"><span data-stu-id="022d1-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="022d1-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="022d1-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="022d1-115">Annuncia l'applicazione per un' [installazione nel contesto di installazione](installation-context.md)per computer.</span><span class="sxs-lookup"><span data-stu-id="022d1-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="022d1-116">In questo modo il pacchetto viene reso disponibile per l'installazione da parte di tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="022d1-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="022d1-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="022d1-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="022d1-118">Annuncia l'applicazione per un'installazione nel [contesto di installazione](installation-context.md)per utente.</span><span class="sxs-lookup"><span data-stu-id="022d1-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="022d1-119">*trasforma*</span><span class="sxs-lookup"><span data-stu-id="022d1-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="022d1-120">Elenco di trasformazioni da applicare al prodotto.</span><span class="sxs-lookup"><span data-stu-id="022d1-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="022d1-121">Le trasformazioni nell'elenco sono delimitate da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="022d1-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="022d1-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="022d1-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="022d1-123">*language*</span><span class="sxs-lookup"><span data-stu-id="022d1-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="022d1-124">Lingua del pacchetto di installazione da usare.</span><span class="sxs-lookup"><span data-stu-id="022d1-124">The language of the installation package to use.</span></span> <span data-ttu-id="022d1-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="022d1-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="022d1-126">*options*</span><span class="sxs-lookup"><span data-stu-id="022d1-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="022d1-127">Opzioni dell'annuncio.</span><span class="sxs-lookup"><span data-stu-id="022d1-127">The advertisement options.</span></span> <span data-ttu-id="022d1-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="022d1-128">This parameter is optional.</span></span> <span data-ttu-id="022d1-129">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="022d1-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="022d1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="022d1-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="022d1-131">Significato</span><span class="sxs-lookup"><span data-stu-id="022d1-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="022d1-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="022d1-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="022d1-133">Annuncio standard</span><span class="sxs-lookup"><span data-stu-id="022d1-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="022d1-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="022d1-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="022d1-135">Annuncia una nuova istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="022d1-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="022d1-136">Richiede che la prima trasformazione nell'elenco di trasformazione del parametro *transforms* sia la trasformazione dell'istanza che modifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="022d1-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="022d1-137">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="022d1-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="022d1-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="022d1-138">Return value</span></span>

<span data-ttu-id="022d1-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="022d1-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="022d1-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="022d1-140">Remarks</span></span>

<span data-ttu-id="022d1-141">Il metodo **AdvertiseProduct** usa la funzione [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="022d1-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="022d1-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="022d1-142">Examples</span></span>

<span data-ttu-id="022d1-143">Nell'esempio seguente viene illustrato l'utilizzo del metodo **AdvertiseProduct** .</span><span class="sxs-lookup"><span data-stu-id="022d1-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="022d1-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="022d1-144">Requirements</span></span>



| <span data-ttu-id="022d1-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="022d1-145">Requirement</span></span> | <span data-ttu-id="022d1-146">Valore</span><span class="sxs-lookup"><span data-stu-id="022d1-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="022d1-147">Versione</span><span class="sxs-lookup"><span data-stu-id="022d1-147">Version</span></span><br/> | <span data-ttu-id="022d1-148">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="022d1-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="022d1-149">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="022d1-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="022d1-150">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="022d1-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="022d1-151">DLL</span><span class="sxs-lookup"><span data-stu-id="022d1-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="022d1-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="022d1-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="022d1-153">IID</span><span class="sxs-lookup"><span data-stu-id="022d1-153">IID</span></span><br/>     | <span data-ttu-id="022d1-154">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="022d1-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="022d1-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="022d1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022d1-156">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="022d1-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="022d1-157">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="022d1-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




