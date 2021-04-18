---
Description: La proprietà ALLUSERS configura il contesto di installazione del pacchetto.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Proprietà ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331617"
---
# <a name="allusers-property"></a><span data-ttu-id="873aa-103">Proprietà ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="873aa-103">ALLUSERS property</span></span>

<span data-ttu-id="873aa-104">La proprietà **ALLUSERS** configura il contesto di installazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="873aa-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="873aa-105">Il Windows Installer esegue un'installazione per utente o per computer a seconda dei privilegi di accesso dell'utente, se sono necessari privilegi elevati per installare l'applicazione, il valore della proprietà **ALLUSERS** , il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) e la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="873aa-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="873aa-106">Il valore della proprietà **ALLUSERS** , al momento dell'installazione, determina il [contesto di installazione](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="873aa-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="873aa-107">Il valore 1 della proprietà **ALLUSERS** specifica il contesto di installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="873aa-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="873aa-108">Il valore della proprietà **ALLUSERS** di una stringa vuota ("") specifica il contesto di installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="873aa-109">Se il valore della proprietà **ALLUSERS** è impostato su 2, il Windows Installer Reimposta sempre il valore della proprietà **ALLUSERS** su 1 ed esegue un'installazione per computer oppure reimposta il valore della proprietà **ALLUSERS** su una stringa vuota ("") ed esegue un'installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="873aa-110">Il valore ALLUSERS = 2 consente al sistema di reimpostare il valore di **ALLUSERS** e il contesto di installazione, a seconda dei privilegi dell'utente e della versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="873aa-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="873aa-111">**Windows 7:** Impostare la proprietà **ALLUSERS** su 2 per utilizzare la proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) per specificare il contesto di installazione.</span><span class="sxs-lookup"><span data-stu-id="873aa-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="873aa-112">Impostare la proprietà **MSIINSTALLPERUSER** su una stringa vuota ("") per un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="873aa-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="873aa-113">Impostare la proprietà **MSIINSTALLPERUSER** su 1 per l'installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="873aa-114">Se il pacchetto è stato scritto seguendo le linee guida per lo sviluppo descritte in [creazione di pacchetti singoli](single-package-authoring.md), gli utenti che dispongono dell'accesso utente possono installare nel contesto per utente senza dover fornire le credenziali di UAC.</span><span class="sxs-lookup"><span data-stu-id="873aa-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="873aa-115">Se l'utente dispone dei privilegi di accesso utente, il programma di installazione esegue un'installazione per computer solo se vengono fornite le credenziali di amministratore alla finestra di dialogo controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="873aa-116">**Windows Vista:** Impostare la proprietà **ALLUSERS** su 2 e Windows Installer conforme a [*controllo dell'account utente*](u-gly.md) (UAC).</span><span class="sxs-lookup"><span data-stu-id="873aa-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="873aa-117">Se l'utente dispone dei privilegi di accesso utente e ALLUSERS = 2, il programma di installazione esegue un'installazione per computer solo se vengono fornite le credenziali di amministratore alla finestra di dialogo controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="873aa-118">Se UAC è abilitato e non vengono fornite le credenziali di amministratore corrette, l'installazione non riesce e viene visualizzato un errore che informa che sono necessari privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="873aa-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="873aa-119">Se UAC è disabilitato dalla chiave del registro di sistema, da criteri di gruppo o dal pannello di controllo, la finestra di dialogo controllo dell'account utente non viene visualizzata e l'installazione ha esito negativo con un errore che informa che sono necessari privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="873aa-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="873aa-120">**Windows XP:** Impostare la proprietà **ALLUSERS** su 2 e Windows Installer esegue un'installazione per utente se l'utente dispone dei privilegi di accesso utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="873aa-121">Se il valore della proprietà **ALLUSERS** non è uguale a 2, il Windows Installer ignora il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) .</span><span class="sxs-lookup"><span data-stu-id="873aa-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="873aa-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="873aa-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="873aa-123">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="873aa-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="873aa-124">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="873aa-124">Default Value</span></span>

<span data-ttu-id="873aa-125">Il contesto di installazione predefinito consigliato è per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="873aa-126">Se **ALLUSERS** non è impostato, il programma di installazione esegue un'installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="873aa-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="873aa-127">È possibile verificare che la proprietà **ALLUSERS** non sia stata impostata impostando il relativo valore su una stringa vuota (""), ALLUSERS = "".</span><span class="sxs-lookup"><span data-stu-id="873aa-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="873aa-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="873aa-128">Remarks</span></span>

<span data-ttu-id="873aa-129">Il [contesto di installazione](installation-context.md) determina i valori delle proprietà [**includevano**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**dei**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**cartellamodelli**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="873aa-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="873aa-130">Il contesto di installazione determina le parti del registro di sistema in cui vengono scritte o rimosse le voci della tabella [del registro di sistema](registry-table.md) e della [tabella RemoveRegistry](removeregistry-table.md), con-1 nella colonna radice.</span><span class="sxs-lookup"><span data-stu-id="873aa-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="873aa-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="873aa-131">Requirements</span></span>



| <span data-ttu-id="873aa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="873aa-132">Requirement</span></span> | <span data-ttu-id="873aa-133">Valore</span><span class="sxs-lookup"><span data-stu-id="873aa-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873aa-134">Versione</span><span class="sxs-lookup"><span data-stu-id="873aa-134">Version</span></span><br/> | <span data-ttu-id="873aa-135">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="873aa-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="873aa-136">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="873aa-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="873aa-137">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="873aa-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="873aa-138">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="873aa-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="873aa-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="873aa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873aa-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="873aa-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="873aa-141">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="873aa-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="873aa-142">Contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="873aa-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="873aa-143">Creazione di pacchetti singoli</span><span class="sxs-lookup"><span data-stu-id="873aa-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




