---
description: L'impostazione della proprietà DISABLEADVTSHORTCUTS Disabilita la generazione di collegamenti che supportano l'installazione su richiesta e l'annuncio. L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti regolari.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Proprietà DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324246"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="31761-104">Proprietà DISABLEADVTSHORTCUTS</span><span class="sxs-lookup"><span data-stu-id="31761-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="31761-105">L'impostazione della proprietà **DISABLEADVTSHORTCUTS** Disabilita la generazione di collegamenti che supportano l' [installazione su richiesta](installation-on-demand.md) e l' [annuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="31761-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="31761-106">L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti regolari.</span><span class="sxs-lookup"><span data-stu-id="31761-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="31761-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="31761-107">Default Value</span></span>

<span data-ttu-id="31761-108">Per impostazione predefinita, la generazione del collegamento di installazione su richiesta è abilitata.</span><span class="sxs-lookup"><span data-stu-id="31761-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="31761-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="31761-109">Remarks</span></span>

<span data-ttu-id="31761-110">I tasti di scelta rapida che supportano l'annuncio hanno il nome di una funzionalità, anziché un percorso di file formattato nel formato \[ \# FileKey \] , immessi nella colonna di destinazione della [tabella dei collegamenti](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="31761-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="31761-111">Se questa proprietà è impostata e la funzionalità è installata, il programma di installazione genera un collegamento normale alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="31761-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="31761-112">Questa proprietà viene comunemente utilizzata dagli amministratori per gli utenti che eseguono il roaming tra ambienti che non supportano la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="31761-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="31761-113">Questa proprietà può essere impostata da una trasformazione, nel flusso amministrativo o nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="31761-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="31761-114">Se viene impostata tramite la riga di comando o tramite una chiamata a [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), è necessario reimpostarla di nuovo durante ogni successiva installazione.</span><span class="sxs-lookup"><span data-stu-id="31761-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="31761-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31761-115">Requirements</span></span>



| <span data-ttu-id="31761-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31761-116">Requirement</span></span> | <span data-ttu-id="31761-117">Valore</span><span class="sxs-lookup"><span data-stu-id="31761-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31761-118">Versione</span><span class="sxs-lookup"><span data-stu-id="31761-118">Version</span></span><br/> | <span data-ttu-id="31761-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31761-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="31761-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31761-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="31761-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31761-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="31761-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="31761-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31761-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31761-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31761-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31761-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




