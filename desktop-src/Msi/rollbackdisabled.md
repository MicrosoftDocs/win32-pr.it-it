---
description: Il programma di installazione imposta la proprietà RollbackDisabled quando il rollback è stato disabilitato.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Proprietà RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326371"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="2712d-103">Proprietà RollbackDisabled</span><span class="sxs-lookup"><span data-stu-id="2712d-103">RollbackDisabled property</span></span>

<span data-ttu-id="2712d-104">Il programma di installazione imposta la proprietà **RollbackDisabled** quando il rollback è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2712d-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="2712d-105">**RollbackDisabled** viene usato dagli autori di pacchetti che devono assicurarsi che il programma di installazione non abbia disabilitato il rollback.</span><span class="sxs-lookup"><span data-stu-id="2712d-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="2712d-106">La proprietà **RollbackDisabled** può essere utilizzata in un'espressione condizionale che rifiuta di continuare con l'installazione se è impostata la proprietà **RollbackDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2712d-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="2712d-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="2712d-107">Default Value</span></span>

<span data-ttu-id="2712d-108">Per impostazione predefinita, il rollback è abilitato.</span><span class="sxs-lookup"><span data-stu-id="2712d-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="2712d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2712d-109">Remarks</span></span>

<span data-ttu-id="2712d-110">Poiché [rollback](rollback-custom-actions.md) e [commit](commit-custom-actions.md) non vengono eseguiti mentre il rollback è disabilitato, il programma di installazione non è in grado di installare correttamente un pacchetto che utilizza questi tipi di azioni personalizzate in una transazione durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2712d-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="2712d-111">In questo caso, l'autore del pacchetto deve includere una condizione che usa DisableRollback che impedisce l'installazione di continuare se il rollback è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2712d-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="2712d-112">Il valore del criterio DisableRollback può essere impostato da un amministratore come parte dell'assegnazione di criteri di sistema.</span><span class="sxs-lookup"><span data-stu-id="2712d-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="2712d-113">Si consiglia agli amministratori di non disabilitare il rollback a meno che non sia necessario.</span><span class="sxs-lookup"><span data-stu-id="2712d-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="2712d-114">Per ulteriori informazioni sul valore del criterio DisableRollback, vedere [criteri di sistema](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="2712d-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2712d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2712d-115">Requirements</span></span>



| <span data-ttu-id="2712d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2712d-116">Requirement</span></span> | <span data-ttu-id="2712d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2712d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2712d-118">Versione</span><span class="sxs-lookup"><span data-stu-id="2712d-118">Version</span></span><br/> | <span data-ttu-id="2712d-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2712d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2712d-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2712d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2712d-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2712d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2712d-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2712d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2712d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2712d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2712d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2712d-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="2712d-125">Rollback dell'installazione</span><span class="sxs-lookup"><span data-stu-id="2712d-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="2712d-126">Criteri di sistema</span><span class="sxs-lookup"><span data-stu-id="2712d-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="2712d-127">rollback delle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="2712d-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="2712d-128">Esegui commit di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="2712d-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




