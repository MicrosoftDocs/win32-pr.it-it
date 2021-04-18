---
description: Il metodo ConfigureProduct dell'oggetto Installer installa o Disinstalla un prodotto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Metodo ureProduct Installer.Config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333883"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="285b5-103">Metodo ureProduct Installer.Config</span><span class="sxs-lookup"><span data-stu-id="285b5-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="285b5-104">Il metodo **ConfigureProduct** dell'oggetto [**Installer**](installer-object.md) installa o Disinstalla un prodotto.</span><span class="sxs-lookup"><span data-stu-id="285b5-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="285b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="285b5-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="285b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="285b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285b5-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="285b5-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="285b5-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="285b5-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="285b5-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="285b5-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="285b5-110">Specifica la configurazione di installazione predefinita del prodotto.</span><span class="sxs-lookup"><span data-stu-id="285b5-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="285b5-111">Il parametro InstallLevel viene ignorato e tutte le funzionalità vengono installate se il parametro InstallState è impostato su un valore diverso da msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="285b5-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="285b5-112">Questo parametro deve essere 0 (installare usando i livelli di funzionalità creati), 65535 (installare tutte le funzionalità) oppure un valore compreso tra 0 e 65535 per installare un subset di funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="285b5-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="285b5-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="285b5-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="285b5-114">Specifica lo stato di installazione per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="285b5-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="285b5-115">Questo parametro deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="285b5-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="285b5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="285b5-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="285b5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="285b5-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="285b5-118"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="285b5-119">La funzionalità è annunciata</span><span class="sxs-lookup"><span data-stu-id="285b5-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="285b5-120"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="285b5-121">La funzionalità viene installata localmente.</span><span class="sxs-lookup"><span data-stu-id="285b5-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="285b5-122"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="285b5-123">La funzionalità viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="285b5-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="285b5-124"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="285b5-125">La funzionalità è installata per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="285b5-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="285b5-126"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="285b5-127">La funzionalità viene installata nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="285b5-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285b5-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="285b5-128">Return value</span></span>

<span data-ttu-id="285b5-129">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="285b5-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="285b5-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="285b5-130">Remarks</span></span>

<span data-ttu-id="285b5-131">Il metodo **ConfigureProduct** Visualizza l'interfaccia utente usando le impostazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="285b5-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="285b5-132">Le impostazioni dell'interfaccia utente possono essere modificate modificando la [**Proprietà UILevel (oggetto Installer)**](installer-uilevel.md) prima di chiamare il metodo **ConfigureProduct** .</span><span class="sxs-lookup"><span data-stu-id="285b5-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="285b5-133">Se il parametro *InstallState* è impostato su un valore diverso da msiInstallStateDefault, il parametro *InstallLevel* viene ignorato e tutte le funzionalità del prodotto sono installate.</span><span class="sxs-lookup"><span data-stu-id="285b5-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="285b5-134">Usare il metodo [**ConfigureFeature**](installer-configurefeature.md) per controllare l'installazione di singole funzionalità quando il parametro *InstallState* non è impostato su msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="285b5-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="285b5-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="285b5-135">Requirements</span></span>



| <span data-ttu-id="285b5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="285b5-136">Requirement</span></span> | <span data-ttu-id="285b5-137">Valore</span><span class="sxs-lookup"><span data-stu-id="285b5-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285b5-138">Versione</span><span class="sxs-lookup"><span data-stu-id="285b5-138">Version</span></span><br/> | <span data-ttu-id="285b5-139">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="285b5-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="285b5-140">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="285b5-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="285b5-141">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="285b5-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="285b5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="285b5-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="285b5-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="285b5-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="285b5-144">IID</span><span class="sxs-lookup"><span data-stu-id="285b5-144">IID</span></span><br/>     | <span data-ttu-id="285b5-145">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="285b5-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="285b5-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="285b5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285b5-147">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="285b5-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="285b5-148">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="285b5-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




