---
description: Il metodo ConfigureFeature dell'oggetto Installer configura lo stato di installazione di una funzionalità del prodotto.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Metodo ureFeature Installer.Config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333882"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="0d721-103">Metodo ureFeature Installer.Config</span><span class="sxs-lookup"><span data-stu-id="0d721-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="0d721-104">Il metodo **ConfigureFeature** dell'oggetto [**Installer**](installer-object.md) configura lo stato di installazione di una funzionalità del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0d721-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d721-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d721-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="0d721-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d721-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d721-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="0d721-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0d721-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0d721-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0d721-109">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="0d721-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="0d721-110">Specifica l'ID funzionalità della funzionalità da configurare.</span><span class="sxs-lookup"><span data-stu-id="0d721-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="0d721-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="0d721-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="0d721-112">Specifica lo stato di installazione per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0d721-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="0d721-113">Questo parametro deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0d721-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="0d721-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0d721-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="0d721-115">Significato</span><span class="sxs-lookup"><span data-stu-id="0d721-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="0d721-116"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="0d721-117">La funzionalità è annunciata</span><span class="sxs-lookup"><span data-stu-id="0d721-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="0d721-118"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="0d721-119">La funzionalità viene installata localmente.</span><span class="sxs-lookup"><span data-stu-id="0d721-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="0d721-120"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="0d721-121">La funzionalità viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="0d721-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="0d721-122"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="0d721-123">La funzionalità è installata per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="0d721-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="0d721-124"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="0d721-125">La funzionalità viene installata nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d721-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d721-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d721-126">Return value</span></span>

<span data-ttu-id="0d721-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0d721-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d721-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d721-128">Requirements</span></span>



| <span data-ttu-id="0d721-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d721-129">Requirement</span></span> | <span data-ttu-id="0d721-130">Valore</span><span class="sxs-lookup"><span data-stu-id="0d721-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d721-131">Versione</span><span class="sxs-lookup"><span data-stu-id="0d721-131">Version</span></span><br/> | <span data-ttu-id="0d721-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d721-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d721-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d721-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d721-134">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d721-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0d721-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0d721-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d721-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d721-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0d721-137">IID</span><span class="sxs-lookup"><span data-stu-id="0d721-137">IID</span></span><br/>     | <span data-ttu-id="0d721-138">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d721-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0d721-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d721-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d721-140">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="0d721-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="0d721-141">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="0d721-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




