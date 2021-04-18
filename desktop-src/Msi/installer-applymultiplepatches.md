---
description: Il metodo ApplyMultiplePatches applica una o più patch ai prodotti idonei per la ricezione della patch. Il metodo imposta la proprietà PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. ApplyMultiplePatches, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328321"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="fc0cc-104">Installer. ApplyMultiplePatches, metodo</span><span class="sxs-lookup"><span data-stu-id="fc0cc-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="fc0cc-105">Il metodo **ApplyMultiplePatches** applica una o più patch ai prodotti idonei per la ricezione della patch.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="fc0cc-106">Il metodo imposta la proprietà [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="fc0cc-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0cc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc0cc-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="fc0cc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc0cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0cc-109">*PatchPackagesList*</span><span class="sxs-lookup"><span data-stu-id="fc0cc-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="fc0cc-110">Stringa che contiene un elenco delimitato da punti e virgola dei percorsi dei file di patch.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="fc0cc-111">Ad esempio: "" c: \\ SUS \\ download \\ cache \\ Office \\ SP1. msp; c: \\ cache di download di SUS \\ \\ \\ Office \\ QFE1. msp; c: \\ SUS \\ download \\ cache \\ Office \\ QFEn. msp ""</span><span class="sxs-lookup"><span data-stu-id="fc0cc-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="fc0cc-112">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="fc0cc-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="fc0cc-113">Questo parametro fornisce il [**ProductCode**](productcode.md) del prodotto a cui viene applicata la patch.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="fc0cc-114">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-114">This parameter is optional.</span></span> <span data-ttu-id="fc0cc-115">Quando questo parametro è null, le patch vengono applicate a tutti i prodotti idonei per la ricezione di tali patch.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="fc0cc-116">*szPropertiesList*</span><span class="sxs-lookup"><span data-stu-id="fc0cc-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="fc0cc-117">Stringa con terminazione null che specifica le impostazioni della proprietà della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="fc0cc-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-118">This parameter is optional.</span></span> <span data-ttu-id="fc0cc-119">Vedere [informazioni sulle proprietà](about-properties.md) e [impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="fc0cc-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="fc0cc-120">Queste proprietà sono condivise da tutti i prodotti di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0cc-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc0cc-121">Return value</span></span>

<span data-ttu-id="fc0cc-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0cc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc0cc-123">Requirements</span></span>



| <span data-ttu-id="fc0cc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc0cc-124">Requirement</span></span> | <span data-ttu-id="fc0cc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fc0cc-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0cc-126">Versione</span><span class="sxs-lookup"><span data-stu-id="fc0cc-126">Version</span></span><br/> | <span data-ttu-id="fc0cc-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc0cc-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc0cc-129">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="fc0cc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fc0cc-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc0cc-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc0cc-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="fc0cc-132">IID</span><span class="sxs-lookup"><span data-stu-id="fc0cc-132">IID</span></span><br/>     | <span data-ttu-id="fc0cc-133">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fc0cc-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="fc0cc-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc0cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0cc-135">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="fc0cc-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="fc0cc-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="fc0cc-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="fc0cc-137">**PATCH**</span><span class="sxs-lookup"><span data-stu-id="fc0cc-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="fc0cc-138">Impostazione dei valori delle proprietà pubbliche nella riga di comando</span><span class="sxs-lookup"><span data-stu-id="fc0cc-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="fc0cc-139">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="fc0cc-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="fc0cc-140">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="fc0cc-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




