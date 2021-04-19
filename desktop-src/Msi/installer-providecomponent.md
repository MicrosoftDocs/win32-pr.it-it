---
description: Il metodo ProvideComponent dell'oggetto Installer restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer. ProvideComponent, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329128"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="e46f5-103">Installer. ProvideComponent, metodo</span><span class="sxs-lookup"><span data-stu-id="e46f5-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="e46f5-104">Il metodo **ProvideComponent** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="e46f5-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="e46f5-105">Se necessario, il metodo **ProvideComponent** dell'oggetto del [**programma di installazione**](installer-object.md) richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e46f5-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="e46f5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e46f5-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="e46f5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e46f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e46f5-108">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="e46f5-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e46f5-109">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e46f5-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="e46f5-110">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="e46f5-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="e46f5-111">Specifica l'ID funzionalità della funzionalità contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="e46f5-112">*Componente*</span><span class="sxs-lookup"><span data-stu-id="e46f5-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="e46f5-113">Specifica il codice del componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="e46f5-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="e46f5-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e46f5-115">Definisce la modalità di installazione.</span><span class="sxs-lookup"><span data-stu-id="e46f5-115">Defines the installation mode.</span></span> <span data-ttu-id="e46f5-116">Questo parametro può essere uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="e46f5-117">Nome</span><span class="sxs-lookup"><span data-stu-id="e46f5-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e46f5-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e46f5-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="e46f5-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="e46f5-120">Fornisce il percorso del componente, eseguendo qualsiasi installazione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="e46f5-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="e46f5-121"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="e46f5-122">Fornisce il percorso del componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="e46f5-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="e46f5-123">Questa modalità verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="e46f5-124"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="e46f5-125">Fornisce il percorso del componente solo se la funzionalità esiste.</span><span class="sxs-lookup"><span data-stu-id="e46f5-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="e46f5-126">In caso contrario, restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="e46f5-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="e46f5-127">Questa modalità controlla la registrazione del componente, ma non verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="e46f5-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="e46f5-129">Fornisce il percorso del componente solo se la funzionalità esiste con un parametro InstallState di *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="e46f5-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="e46f5-130">Questa operazione Controlla la registrazione del componente, ma non verifica l'esistenza del file di chiave del componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="e46f5-131"><dt>**combinazione dei flag msiReinstallMode**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="e46f5-132">Chiama [**ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità utilizzando questo parametro per il parametro *REINSTALLMODE* e quindi fornisce il componente.</span><span class="sxs-lookup"><span data-stu-id="e46f5-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e46f5-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e46f5-133">Return value</span></span>

<span data-ttu-id="e46f5-134">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e46f5-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e46f5-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="e46f5-135">Remarks</span></span>

<span data-ttu-id="e46f5-136">Il metodo **ProvideComponent** combina le funzionalità di [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)e [**ComponentPath**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="e46f5-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="e46f5-137">Il metodo **ProvideComponent** semplifica la sequenza chiamante, ma incrementa anche il conteggio di utilizzo e deve essere usato con cautela per evitare conteggi di utilizzo non accurati.</span><span class="sxs-lookup"><span data-stu-id="e46f5-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="e46f5-138">Il metodo **ProvideComponent** offre anche una minore flessibilità rispetto a una serie di singole chiamate ai metodi e alle proprietà citate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e46f5-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="e46f5-139">Se l'applicazione esegue il ripristino da una situazione imprevista, è probabile che l'applicazione abbia già chiamato [**UseFeature**](installer-usefeature.md) e abbia incrementato il numero di utilizzi.</span><span class="sxs-lookup"><span data-stu-id="e46f5-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="e46f5-140">In questo caso, l'applicazione deve evitare di incrementare il conteggio di utilizzo chiamando il metodo [**ConfigureFeature**](installer-configurefeature.md) anziché il metodo **ProvideComponent** .</span><span class="sxs-lookup"><span data-stu-id="e46f5-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="e46f5-141">Non è possibile usare l'opzione msiInstallModeExisting in combinazione con i flag msiReinstallMode.</span><span class="sxs-lookup"><span data-stu-id="e46f5-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="e46f5-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e46f5-142">Requirements</span></span>



| <span data-ttu-id="e46f5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e46f5-143">Requirement</span></span> | <span data-ttu-id="e46f5-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e46f5-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e46f5-145">Versione</span><span class="sxs-lookup"><span data-stu-id="e46f5-145">Version</span></span><br/> | <span data-ttu-id="e46f5-146">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e46f5-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e46f5-147">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e46f5-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e46f5-148">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e46f5-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e46f5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e46f5-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="e46f5-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e46f5-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e46f5-151">IID</span><span class="sxs-lookup"><span data-stu-id="e46f5-151">IID</span></span><br/>     | <span data-ttu-id="e46f5-152">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e46f5-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e46f5-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e46f5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e46f5-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="e46f5-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




