---
description: La proprietà MSIRESTARTMANAGERCONTROL specifica se il pacchetto Windows Installer utilizza la funzionalità di gestione riavvio o della finestra di dialogo FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Proprietà MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331082"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="c53ca-103">Proprietà MSIRESTARTMANAGERCONTROL</span><span class="sxs-lookup"><span data-stu-id="c53ca-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="c53ca-104">La proprietà **MSIRESTARTMANAGERCONTROL** specifica se il pacchetto Windows Installer utilizza la funzionalità di [Gestione riavvio](../rstmgr/restart-manager-portal.md) o della [finestra di dialogo FilesInUse](filesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c53ca-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="c53ca-105">Valore</span><span class="sxs-lookup"><span data-stu-id="c53ca-105">Value</span></span>



| <span data-ttu-id="c53ca-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c53ca-106">Value</span></span>                                                                                        | <span data-ttu-id="c53ca-107">Significato</span><span class="sxs-lookup"><span data-stu-id="c53ca-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c53ca-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c53ca-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="c53ca-109">Si tratta del valore predefinito se la proprietà non è impostata.</span><span class="sxs-lookup"><span data-stu-id="c53ca-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="c53ca-110">Windows Installer tenta sempre di utilizzare [Gestione riavvio](../rstmgr/restart-manager-portal.md) in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c53ca-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c53ca-111"><dt>Disabilitare</dt></span><span class="sxs-lookup"><span data-stu-id="c53ca-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="c53ca-112">Disabilita l'interazione del pacchetto con [Gestione riavvio](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c53ca-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="c53ca-113">Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c53ca-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="c53ca-114"><dt>DisableShutdown</dt></span><span class="sxs-lookup"><span data-stu-id="c53ca-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="c53ca-115">Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c53ca-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="c53ca-116">Questa impostazione Disabilita i tentativi da parte di [Gestione riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii durante l'installazione di un pacchetto di Windows Installer che non è stato creato per usare Gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="c53ca-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="c53ca-117">Il programma di installazione utilizza ancora Gestione riavvio per rilevare i file utilizzati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c53ca-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c53ca-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c53ca-118">Remarks</span></span>

<span data-ttu-id="c53ca-119">La proprietà **MSIRESTARTMANAGERCONTROL** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c53ca-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="c53ca-120">Il valore di questa proprietà può essere modificato usando le trasformazioni di personalizzazione o gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="c53ca-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="c53ca-121">La modifica del valore di questa proprietà da azioni personalizzate non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="c53ca-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c53ca-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c53ca-122">Requirements</span></span>



| <span data-ttu-id="c53ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c53ca-123">Requirement</span></span> | <span data-ttu-id="c53ca-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c53ca-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c53ca-125">Versione</span><span class="sxs-lookup"><span data-stu-id="c53ca-125">Version</span></span><br/> | <span data-ttu-id="c53ca-126">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c53ca-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c53ca-127">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c53ca-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c53ca-128">Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c53ca-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c53ca-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c53ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53ca-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c53ca-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c53ca-131">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="c53ca-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="c53ca-132">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="c53ca-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
