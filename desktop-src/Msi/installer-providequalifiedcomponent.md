---
description: Il metodo ProvideQualifiedComponent dell'oggetto Installer restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie. Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. ProvideQualifiedComponent, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329127"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="a3225-104">Installer. ProvideQualifiedComponent, metodo</span><span class="sxs-lookup"><span data-stu-id="a3225-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="a3225-105">Il metodo **ProvideQualifiedComponent** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="a3225-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="a3225-106">Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a3225-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3225-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3225-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="a3225-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3225-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3225-109">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="a3225-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="a3225-110">Specifica l'ID componente per il componente richiesto.</span><span class="sxs-lookup"><span data-stu-id="a3225-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="a3225-111">Potrebbe non essere il GUID per il componente stesso, bensì un server che fornisce la funzionalità corretta, come nella colonna ComponentId della [tabella PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3225-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3225-112">*Qualifier*</span><span class="sxs-lookup"><span data-stu-id="a3225-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a3225-113">Specifica un qualificatore in un elenco di componenti pubblicitari (dalla [tabella PublishComponent](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="a3225-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a3225-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="a3225-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="a3225-115">Definisce la modalità di installazione.</span><span class="sxs-lookup"><span data-stu-id="a3225-115">Defines the installation mode.</span></span> <span data-ttu-id="a3225-116">Questo parametro può essere uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a3225-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="a3225-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="a3225-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="a3225-118">Significato</span><span class="sxs-lookup"><span data-stu-id="a3225-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="a3225-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3225-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="a3225-120">Fornisce il componente, eseguendo le installazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="a3225-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="a3225-121"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="a3225-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="a3225-122">Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="a3225-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="a3225-123">Questa modalità verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="a3225-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="a3225-124"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="a3225-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="a3225-125">Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="a3225-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="a3225-126">Questa modalità controlla solo che il componente sia registrato, ma non verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="a3225-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="a3225-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="a3225-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="a3225-128">Fornisce il percorso del componente solo se la funzionalità esiste con un parametro InstallState di *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="a3225-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="a3225-129">Questa operazione Controlla la registrazione del componente, ma non verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="a3225-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="a3225-130"><dt>**combinazione dei flag msiReinstallMode**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3225-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="a3225-131">Chiama [**ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità utilizzando questo parametro per il parametro *REINSTALLMODE* e quindi fornisce il componente.</span><span class="sxs-lookup"><span data-stu-id="a3225-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3225-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3225-132">Return value</span></span>

<span data-ttu-id="a3225-133">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a3225-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3225-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3225-134">Requirements</span></span>



| <span data-ttu-id="a3225-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3225-135">Requirement</span></span> | <span data-ttu-id="a3225-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a3225-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3225-137">Versione</span><span class="sxs-lookup"><span data-stu-id="a3225-137">Version</span></span><br/> | <span data-ttu-id="a3225-138">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3225-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a3225-139">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3225-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a3225-140">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3225-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a3225-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a3225-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3225-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3225-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a3225-143">IID</span><span class="sxs-lookup"><span data-stu-id="a3225-143">IID</span></span><br/>     | <span data-ttu-id="a3225-144">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a3225-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="a3225-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3225-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3225-146">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="a3225-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




