---
description: Il metodo ProvideAssembly dell'oggetto Installer restituisce il percorso installato di un assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Programma di installazione::P metodo rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332174"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="f5b77-103">Programma di installazione::P metodo rovideAssembly</span><span class="sxs-lookup"><span data-stu-id="f5b77-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="f5b77-104">Il metodo **ProvideAssembly** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso installato di un assembly.</span><span class="sxs-lookup"><span data-stu-id="f5b77-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5b77-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="f5b77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b77-107">*assembly*</span><span class="sxs-lookup"><span data-stu-id="f5b77-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b77-108">Nome sicuro dell'assembly installato su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="f5b77-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="f5b77-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="f5b77-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b77-110">Impostare su null per gli assembly globali.</span><span class="sxs-lookup"><span data-stu-id="f5b77-110">Set to null for global assemblies.</span></span> <span data-ttu-id="f5b77-111">Per gli assembly privati, impostare *appContext* sul percorso completo del file di configurazione dell'applicazione o sul percorso completo del file eseguibile dell'applicazione in cui l'assembly è stato reso privato.</span><span class="sxs-lookup"><span data-stu-id="f5b77-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="f5b77-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="f5b77-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b77-113">Definisce la modalità di installazione.</span><span class="sxs-lookup"><span data-stu-id="f5b77-113">Defines the installation mode.</span></span> <span data-ttu-id="f5b77-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5b77-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f5b77-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b77-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="f5b77-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f5b77-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="f5b77-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="f5b77-118">Fornire il componente ed eseguire qualsiasi installazione necessaria per fornire il componente.</span><span class="sxs-lookup"><span data-stu-id="f5b77-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="f5b77-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="f5b77-120">Fornire il componente solo se la funzionalità esiste.</span><span class="sxs-lookup"><span data-stu-id="f5b77-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="f5b77-121">Questa opzione consente di verificare che l'assembly esista.</span><span class="sxs-lookup"><span data-stu-id="f5b77-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="f5b77-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="f5b77-123">Fornire il componente solo se la funzionalità esiste.</span><span class="sxs-lookup"><span data-stu-id="f5b77-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="f5b77-124">Questa opzione non verifica che l'assembly esista.</span><span class="sxs-lookup"><span data-stu-id="f5b77-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="f5b77-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="f5b77-126">Fornisce l'assembly solo se l'assembly è installato localmente.</span><span class="sxs-lookup"><span data-stu-id="f5b77-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="f5b77-127"><dt>**Combinazione dei flag utilizzati da [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="f5b77-128">Chiama il metodo [**ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità utilizzando questo parametro per *REINSTALLMODE* e quindi restituisce il percorso dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="f5b77-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f5b77-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="f5b77-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b77-130">Informazioni sull'assembly e tipo di assembly.</span><span class="sxs-lookup"><span data-stu-id="f5b77-130">Assembly information and assembly type.</span></span> <span data-ttu-id="f5b77-131">Impostare su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5b77-131">Set to one of the following values.</span></span>



| <span data-ttu-id="f5b77-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b77-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="f5b77-133">Significato</span><span class="sxs-lookup"><span data-stu-id="f5b77-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="f5b77-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="f5b77-135">Assembly .NET.</span><span class="sxs-lookup"><span data-stu-id="f5b77-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="f5b77-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f5b77-137">Assembly affiancato Win32.</span><span class="sxs-lookup"><span data-stu-id="f5b77-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b77-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5b77-138">Return value</span></span>

<span data-ttu-id="f5b77-139">Percorso dell'assembly installato.</span><span class="sxs-lookup"><span data-stu-id="f5b77-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b77-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5b77-140">Remarks</span></span>

<span data-ttu-id="f5b77-141">Il metodo **ProvideAssembly** usa la funzione [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="f5b77-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="f5b77-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5b77-142">Examples</span></span>

<span data-ttu-id="f5b77-143">Lo script di esempio seguente illustra l'uso del Metodo ProvideAssembly.</span><span class="sxs-lookup"><span data-stu-id="f5b77-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="f5b77-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5b77-144">Requirements</span></span>



| <span data-ttu-id="f5b77-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b77-145">Requirement</span></span> | <span data-ttu-id="f5b77-146">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b77-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b77-147">Versione</span><span class="sxs-lookup"><span data-stu-id="f5b77-147">Version</span></span><br/> | <span data-ttu-id="f5b77-148">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5b77-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f5b77-149">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f5b77-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f5b77-150">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5b77-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="f5b77-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b77-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5b77-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b77-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="f5b77-153">IID</span><span class="sxs-lookup"><span data-stu-id="f5b77-153">IID</span></span><br/>     | <span data-ttu-id="f5b77-154">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f5b77-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="f5b77-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5b77-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b77-156">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="f5b77-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="f5b77-157">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="f5b77-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




