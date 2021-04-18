---
description: Le proprietà MSIINSTALLPERUSER e ALLUSERS possono essere impostate dall'utente al momento dell'installazione, tramite l'interfaccia utente o la riga di comando, per richiedere che l'Windows Installer installare un pacchetto a doppio scopo per l'utente corrente o per tutti gli utenti del computer.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Proprietà MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325464"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="532e5-103">Proprietà MSIINSTALLPERUSER</span><span class="sxs-lookup"><span data-stu-id="532e5-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="532e5-104">Le proprietà **MSIINSTALLPERUSER** e [**ALLUSERS**](allusers.md) possono essere impostate dall'utente al momento dell'installazione, tramite l'interfaccia utente o la riga di comando, per richiedere che l'Windows Installer installare un pacchetto a doppio scopo per l'utente corrente o per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="532e5-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="532e5-105">Per usare la proprietà **MSIINSTALLPERUSER** , il valore della proprietà [**ALLUSERS**](allusers.md) deve essere 2 e il pacchetto deve essere stato creato per essere in grado di eseguire l'installazione in un contesto per utente o per computer.</span><span class="sxs-lookup"><span data-stu-id="532e5-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="532e5-106">Per informazioni sulla creazione di un pacchetto a doppio scopo, vedere [creazione di pacchetti singoli](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="532e5-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="532e5-107">Se il valore della proprietà **ALLUSERS** non è uguale a 2, il valore della proprietà **MSIINSTALLPERUSER** viene ignorato e non ha alcun effetto sull'installazione.</span><span class="sxs-lookup"><span data-stu-id="532e5-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="532e5-108">Il valore della proprietà **MSIINSTALLPERUSER** viene ignorato quando si installa il pacchetto utilizzando Windows Installer 4,5 o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="532e5-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="532e5-109">Per richiedere che l'Windows Installer installi il pacchetto a doppio scopo nel contesto di [installazione](installation-context.md)per computer, l'utente può impostare il valore della proprietà **MSIINSTALLPERUSER** su una stringa vuota ("") e il valore della proprietà [**ALLUSERS**](allusers.md) su 2 usando un'interfaccia utente creata o una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="532e5-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="532e5-110">Per richiedere che l'Windows Installer installi il pacchetto a doppio scopo nel contesto di [installazione](installation-context.md)per utente, l'utente può impostare il valore della proprietà **MSIINSTALLPERUSER** su 1 e il valore della proprietà [**ALLUSERS**](allusers.md) su 2 usando un'interfaccia utente creata o una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="532e5-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="532e5-111">Se il valore della proprietà [**ALLUSERS**](allusers.md) non è uguale a 2, il Windows Installer ignora il valore della proprietà **MSIINSTALLPERUSER** .</span><span class="sxs-lookup"><span data-stu-id="532e5-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="532e5-112">Se Windows Installer installa l'applicazione nel contesto per computer, reimposta il valore della proprietà **ALLUSERS** su 1.</span><span class="sxs-lookup"><span data-stu-id="532e5-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="532e5-113">Se Windows Installer installa l'applicazione nel contesto per utente, reimposta il valore della proprietà **ALLUSERS** su una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="532e5-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="532e5-114">Le applicazioni installate per utente ricevono quindi tutti gli aggiornamenti o le riparazioni per ogni utente e le applicazioni installate per computer ricevono aggiornamenti o riparazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="532e5-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="532e5-115">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** la proprietà **MSIINSTALLPERUSER** viene ignorata dalle versioni precedenti a Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="532e5-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="532e5-116">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="532e5-116">Default Value</span></span>

<span data-ttu-id="532e5-117">Il contesto di installazione predefinito consigliato è per utente per un pacchetto a doppio scopo.</span><span class="sxs-lookup"><span data-stu-id="532e5-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="532e5-118">Creare MSIINSTALLPERUSER = 1 e ALLUSERS = 2 nella [tabella delle proprietà](property-table.md) del pacchetto a doppio scopo per specificare per utente come contesto di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="532e5-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="532e5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="532e5-119">Remarks</span></span>

<span data-ttu-id="532e5-120">È possibile verificare che la proprietà **MSIINSTALLPERUSER** non sia stata impostata impostando il relativo valore su una stringa vuota (""), MSIINSTALLPERUSER = "".</span><span class="sxs-lookup"><span data-stu-id="532e5-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="532e5-121">Il contesto di installazione determina i valori delle proprietà [**includevano**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**dei**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**cartellamodelli**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="532e5-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="532e5-122">Il contesto di installazione determina le parti del registro di sistema in cui vengono scritte o rimosse le voci della tabella [del registro di sistema](registry-table.md) e della [tabella RemoveRegistry](removeregistry-table.md), con-1 nella colonna radice.</span><span class="sxs-lookup"><span data-stu-id="532e5-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="532e5-123">Per informazioni sul contesto di installazione, vedere [contesto di installazione](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="532e5-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="532e5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="532e5-124">Requirements</span></span>



| <span data-ttu-id="532e5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="532e5-125">Requirement</span></span> | <span data-ttu-id="532e5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="532e5-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="532e5-127">Versione</span><span class="sxs-lookup"><span data-stu-id="532e5-127">Version</span></span><br/> | <span data-ttu-id="532e5-128">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="532e5-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="532e5-129">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="532e5-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="532e5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="532e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="532e5-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="532e5-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="532e5-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="532e5-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="532e5-133">Contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="532e5-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="532e5-134">Creazione di pacchetti singoli</span><span class="sxs-lookup"><span data-stu-id="532e5-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




